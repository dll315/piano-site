# 钢琴音乐站

一个可直接弹奏、也支持自动弹奏的钢琴网页。内置四首曲目：

- 把回忆拼好给你
- 精卫（30 年前，50 年后）
- 青花瓷
- 觉悟（王小帅）

手动弹奏与自动弹奏均带有按键、下落音符、光晕和粒子特效，并支持鼠标、触摸和电脑键盘演奏。

## Docker 部署

### 方式一：docker compose

```bash
docker compose up -d --build
```

访问 `http://localhost:8084`。

### 方式二：直接构建运行

```bash
docker build -t piano-site .
docker run -d --name piano-site -p 8084:80 --restart unless-stopped piano-site
```

访问 `http://localhost:8084`。

### 健康检查

```bash
curl http://localhost:8084/healthz
```

返回 `ok` 表示服务正常。

## 本地运行

直接用浏览器打开 `index.html` 即可。
