   跨平台(windows macos linux)的环境变量设置工具 yarn add cross-env -D
   在nodejs中设置的环境变量的获取 process.env.[key] 类似于浏览器的window对象
   通过npm run start脚本运行时设置process.env.NODE_ENV === "development" 表示项目处于开发阶段可以使用console.log、alert
1. 安装依赖 husky
   yarn add husky-init -D
   yarn add husky -D
   npx husky-init
2. 提交拦截器
   在pre-commit文件中将npm test替换为 npx eslint --fix ./src --ext .js,.jsx,.ts,tsx
3. 提交步骤
   git add   /git add .
   git commit -m '提交的信息'
4. 配置 lint-staged
   1 yarn add lint-staged -D
   2 在package.json文件添加
      "lint-staged": {
        "*.{js,jsx,ts,tsx}": "npx eslint --fix"
      },
   3 在pre-commit文件中将npx eslint --fix ./src --ext .js,.jsx,.ts,tsx替换为 npx lint-staged

5. 仓库提交
git status
