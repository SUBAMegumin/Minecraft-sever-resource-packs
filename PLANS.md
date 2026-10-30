# 发布规划

目标：发布Infernal HUD 1.6.0完整ZIP与固定版本Release直链。复用已验收原包，不重做图片、不修改SHA1。

工作区与资源管理：packs/保存892110字节公开包，docs/保存发布/验证记录，.github/workflows/保存自动发布；根目录仅README/AGENTS/PLANS及忽略规则。初始为空仓库，新文件预算1MiB（不含Git对象）；保留带版本资源以维持旧链接。发布者负责清理自己产生的可再生临时文件，现无大型测试环境。每轮验收git status和体积；不拷贝服务端、依赖缓存或私有工程。

实施：推送main及infernal-hud-1.6.0标签，Actions检查哈希并上传Release；检查匿名公网GET、ZIP与SHA1，区分直连和代理。禁止提前把未验证直链称为可用。
