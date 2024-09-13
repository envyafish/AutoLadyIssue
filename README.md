# AutoLadyIssue
收集issue
### 食用方法
```
docker run
  -d
  --name='auto-lady'
  --net='bridge'
  -p 8043:80
  -v /mnt/user/appdata/auto-lady:/data 
  /orekiiiiiiiiiiiii/auto-lady:latest
```

```
version: '3'
services:
  auto-lady:
    image: orekiiiiiiiiiiiii/auto-lady:latest
    container_name: auto-lady
    restart: always
    networks:
      - bridge
    ports:
      - "8043:80"
    volumes:
      - /mnt/user/appdata/auto-lady:/data

networks:
  bridge:
    driver: bridge
```
首次启动 账号密码可在后台日志查看
