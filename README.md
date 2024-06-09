# Next.js 官方教程学习总结
## 课程
[官方课程地址](https://nextjs.org/learn)
[官方课程代码的github地址](https://github.com/vercel/next-learn)

[Learn Next.js中文教程](https://qufei1993.github.io/nextjs-learn-cn/)

### 密码

user@nextmail.com

123456

## 知识总结

### 第1章 创建项目

创建项目

``` terminal
npx create-next-app@latest nextjs-dashboard --use-npm --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example"
```

### 第2章 css

使用tailwindcss

### 第3章 优化字体和图片

使用nextjs的<Image>组件而不是原生的<img>

使用className="hidden md:block"和className="block md:hidden"进行pc端和移动端的图片适配，表示在宽度大于768px时显示pc端的图片而在小于768px时显示移动端的图片

### 第4章 创建layouts和pages

使用嵌套路由

### 第5章 在页面间跳转

使用<Link />而不是<a>从而避免全页面的刷新

使用usePathname()来获取当前页面的路径

在className中使用clsx

### 第6章 设置数据库

使用vercel的postgresSQL数据库

在.gitignore文件中确保.env文件在忽略文件中

使用npm run seed初始化数据库的数据

### 第7章 拉取数据

使用服务器组件获取数据

### 第8章 静态渲染和动态渲染

为了使仪表盘数据动态化，需要在server components中使用unstable_noStore，防止response被缓存

### 第9章 Streaming

流式传输可以防止缓慢的数据请求阻塞整个页面。

使用loading.tsx来完成流式传输

在loading.tsx中使用骨架屏

使用流式处理组件：

使用`<Suspense>` 将`<RevenueChart />`包裹起来， 并向其传递一个名为 `<RevenueChartSkeleton>` 的回退组件

 Suspense是一个很强大的API

### 第10章 部分预渲染

### 第11章 添加搜索和分页

为什么使用URL搜索参数？

1. 可添加书签和可共享的URL
2. 服务端渲染和初始加载
3. 分析和跟踪

使用useSearchParams，usePathname和useRouter

使用replace方法

defaultValue vs value

如果使用state来管理输入的值，使用value让其成为受控组件。

如果没有用state，可以使用defaultValue，原生输入框将管理自己的状态

使用use-debounce来防抖

在pagination.tsx组件中处理分页

### 第12章 更改数据

使用server action

使用zod进行类型验证

使用revalidatePath触发新请求

使用redirect进行重定向

使用params获取数据

使用Promise.all并行发请求

### 第13章 处理错误

在server action中使用服务器操作

使用error.tsx处理错误

使用noutFound处理404

### 第14章 提高可访问性

服务器端验证，使用aria标签

### 第15章 添加身份验证

Authentication: 身份验证

Authorization: 授权

使用NextAuth.js

### 第16章 添加元数据

元数据：增强网页的seo

使用Metadata























