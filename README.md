# elastalert-dingtalk-plugin

## 安装
```
sudo apt install -y  python-pip python-dev libffi-dev libssl-dev
sudo pip install -r requirements.txt 
```

## 修改配置:
 `config.yaml`:

 * `es_host`: elasticsearch 地址
 * `es_port`: elasticsearch 端口 

## 修改添加报警规则
 启用钉钉的报警，需添加必要的配置, 例如

```
alert:
- dingtalk 

dingtalk_webhook: your-dingtalk-robot-webhook-url
dingtalk_msgtype: text
```

报警规则在`rules`目录中，可以随意的添加格式报警规则
  
## 创建警报的index:

```
    elastalert-create-index --index elastalert_status --old-index 
```

## 运行:

```
python -m elastalert.elastalert --verbose
```
