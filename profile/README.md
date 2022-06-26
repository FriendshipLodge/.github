## 项目命名规范
 - 前端:frontend_项目名
 - 后端:backend_项目名

## 版本分支
 - master:主分支，进行版本发布分支，不在该分支上进行开发。
 - hotfixes:修补分支，进行紧急bug修补分支。
 - dev_[name]:各自开发人员的开发分支，当进行代码提交时需要合并到主分支时创建pull request请求合并，
              Git Actions执行自动化测试后未产生代码冲突，由管理员同意合并。
   
## CI/CD 采用GitOps流程
 - 代码合并master分支之后，由GitActions执行脚本，创建docker镜像存储在github仓库，由K8s自动拉取更新生产环境版本
