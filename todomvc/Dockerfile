# 使用官方的 Node.js 镜像作为基础镜像
FROM node:8.17.0-alpine 

# 设置工作目录  
WORKDIR /app  

# 设置环境变量，用于配置npm镜像（可选）  
#ARG NPM_REGISTRY=https://registry.npm.taobao.org  
#RUN npm config set registry $NPM_REGISTRY  

# 复制 package.json 和 package-lock.json  
COPY package*.json ./  

# 更新 npm 到最新版本
RUN npm install -g npm@latest

# 安装依赖  
RUN npm install --no-cache

# 复制应用代码
COPY . .

# 构建应用
RUN npm run build

# 暴露应用运行的端口
EXPOSE 80

# 启动应用
CMD ["npm", "start"]
