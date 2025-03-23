## 项目名称：PhotoSite
#### 项目概述
PhotoSite 是一个用于上传、管理、展示图片或图集的网站。用户可以通过该平台方便地分享和管理自己的照片和图集，与其他用户互动交流。

#### 核心功能
##### 1. 用户系统
注册与登录：用户需要通过邮箱验证以及使用邀请码来创建账户。
邮箱验证：注册时发送验证链接或验证码到用户的注册邮箱，确保用户身份的有效性。
邀请码：引入邀请码机制，没有邀请码的用户无法创建账户。
登录与权限：访问本网站是必须先登录的，只有通过邮箱验证并成功登录的用户才能使用其他功能。
##### 2. 上传功能
照片管理：用户可以上传、编辑和删除自己的照片。
批量上传：支持一次性上传多张照片到图集。
照片编辑：提供基本的图片编辑功能，如裁剪、旋转、滤镜等（可以使用Canvas API或集成Sharp库）。
存储优化：自动生成缩略图（可以使用FFmpeg或其他图像处理工具），原始图和缩略图分开存储。
##### 3. 标签系统
标签自动推荐：根据用户输入的历史标签或热门标签提供补全建议。
标签管理后台：允许管理员合并重复标签、删除无效标签。
标签云展示：在搜索页展示热门标签的视觉化标签云。
##### 4. 图集功能
图集封面设置：用户可以选择图集中的某张照片作为封面。
图集分类：支持自定义标签，并按标签分类展示图集。
图集可见性：提供公开/私密/仅限关注者访问的权限控制。
##### 5. 搜索功能增强
高级过滤：用户可以根据上传时间、点赞数、标签等进行筛选。
分页与懒加载：避免一次性加载过多数据，提升性能。
搜索历史记录：记录用户最近搜索的关键词，方便快速回溯。\

#### 用户体验优化
##### 1. 交互设计
拖拽上传：实现类似Google Drive的拖拽文件上传体验。
上传进度条：实时显示上传进度和剩余时间。
操作反馈：提供成功/失败的提示信息（如“上传完成”或“文件过大”）。
##### 2. 内容展示
瀑布流布局：搜索页采用Pinterest式的瀑布流展示缩略图。
图片懒加载：滚动到可视区域再加载图片（使用Intersection Observer API）。
图片查看器：支持缩放、旋转、下载
键盘导航：支持方向键切换焦点、回车查看详情。
##### 3. 社交互动
点赞/收藏：用户可以对照片或图集点赞或收藏。
评论系统：允许用户对照片发表评论，并支持@他人和表情符号。
关注功能：用户可以关注其他用户，并在首页看到关注者的新内容。

#### 安全与性能
##### 1. 安全防护
文件类型限制：仅允许上传JPG/PNG等格式，防止恶意文件上传。
##### 2. 性能优化
数据库索引：为照片标题、标签、上传时间等字段建立索引，优化搜索速度。

#### 进阶功能
##### 1. 管理员后台
数据看板：统计活跃用户、上传量、热门标签等数据。
内容管理：删除违规内容、封禁用户、审核新注册用户。
##### 2. 移动端适配
响应式设计：确保在手机、平板、桌面端均有良好的显示效果。

#### 技术栈
前端：React + TypeScript + Tailwind CSS（组件库如Ant Design）
后端：Node.js (Express) + MySQL + Elasticsearch
存储：本地磁盘存储，无需AWS S3
监控：Sentry（错误跟踪） + Prometheus（性能监控）
开发与部署
先在本地电脑上开发，完成后再部署到服务器上测试。
先实现核心功能（用户系统 + 上传 + 搜索），再逐步迭代其他模块。
善用第三方库，如Canvas API、Sharp等，提升用户体验。
善用文档和示例，快速上手新技术。#   P h o t o S i t e  
 