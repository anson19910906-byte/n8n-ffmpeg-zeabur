# 步驟 1: 使用官方的 n8n 映像檔作為基礎
FROM n8nio/n8n

# 步驟 2: 切換到 root 使用者以獲得安裝權限
USER root

# 步驟 3: 更新套件列表並安裝 ffmpeg
RUN apt-get update && apt-get install -y ffmpeg && rm -rf /var/lib/apt/lists/*

# 步驟 4: 切換回 n8n 預設的非 root 使用者
USER node

# 步驟 5: (最終修正) 強制設定容器的進入點為 n8n
ENTRYPOINT ["n8n"]
