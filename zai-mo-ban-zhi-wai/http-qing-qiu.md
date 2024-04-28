# http请求

由于单纯的模板渲染无法进行脚本操作，比如一个简单的却需要向服务器发送请求的**文章点赞**，因此sonic提供了接口以便于完成类似的操作。

在[`github.com/go-sonic/sonic/handler/router.go`](https://github.com/go-sonic/sonic/blob/master/handler/router.go#L311)这个路由注册文件中可以找到，这些接口都采用简单的RESTful风格。

由于接口随时会变动（其实是生吃代码的巅峰期过了），虽然是主题开发一个重要部分，但这里就不花更多精力一一讲解各个接口的作用，有需要请自行阅读这部分源码。

至于在模板中调用http请求接口，可以参考默认主题中的做法：

```html
 <!--index.tmpl中调用脚本模板 -->
 {{template "caicai_anatole/module/post-likes/scripts" .}}
```

脚本中使用了[Alpine.js](https://www.alpinejs.cn/)轻量框架与[XMLHttpRequest](https://developer.mozilla.org/zh-CN/docs/Web/API/XMLHttpRequest)

```html
<!--module/post-likes/scripts.tmpl中定义脚本模板 -->
{{- define "caicai_anatole/module/post-likes/scripts" -}}
<script>
    document.addEventListener("alpine:init", () => {
        Alpine.data("posts", () => ({
            likedIds: [],
            init() {
                this.likedIds = JSON.parse(localStorage.getItem("anatole.likes.post.ids") || "[]");
            },
            liked(id) {
                return this.likedIds.includes(id);
            },
            async handleLike(postId) {
                if (this.liked(postId)) {
                    return
                }

                const xhr = new XMLHttpRequest();

                xhr.open('POST', "/api/content/posts/" + postId + "/likes");

                xhr.onload = () => {
                    this.likedIds = [...this.likedIds, postId];
                    localStorage.setItem('anatole.likes.post.ids', JSON.stringify(this.likedIds));

                    const likesNode = document.querySelector("[data-post-id-likes=\"" + postId + "\"]");
                    const likes = parseInt(likesNode.innerText);
                    likesNode.innerText = likes + 1;
                }
                xhr.onerror = function () {
                    alert("网络请求失败，请稍后再试");
                };
                xhr.send();
            }
        }))
    })
</script>
{{end}}
```
