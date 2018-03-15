# 美化版 Nginx 目录浏览界面

## 使用方法

### 在对应 `server` 段的 `conf` 文件中，添加 `autoindex` 参数 
```
server {	
    listen			80;
	server_name  	test.com;
	root			/path/;

	autoindex                  on;    # 显示目录
	autoindex_format         json;    # JSON 形式返回目录结构
	autoindex_exact_size       on;    # 显示文件大小
	autoindex_localtime        on;    # 显示文件时间
}

```

### 上传 `auto.html` 到根目录 `/path/` 

确保 test.com/auto.html 可以正常访问


### 完成！