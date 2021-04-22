# PyFly



#### 软件架构
1.前端模板：[Layui Fly Template](http://www.layui.com/template/fly/)

2.Flask + flask-pymongo + flask-admin + flask-login + flask-mail



#### 安装教程

```shell


#安装MongoDB

#创建虚拟环境： (3.6)
conda create -n py36 python==3.6

# 激活虚拟环境：
activate py36
#  安装依赖
pip install -r requirements.txt
# 运行项目
python manager.py runserver
```

##### 测试账号： 

```
user:admin
pwd:admin
```



#### 使用说明

1. 首次打开会自动往MongoDB新增一些默认数据（管理员账号和默认配置项），后台管理（flask-admin简单实现）: http://127.0.0.1:5000/admin

2. 可自己修改扩展模板作为信息分类网站或者简单的cms、博客

3.图片上传可选保存到后端或图床，默认保存到服务器，如果要开启图床上传在/static/js/mods/index.js搜索开启图床注释和解开相应注释后即可，然后在user.js进行相应操作，图床使用了[SM.MS图床](http://sm.ms)

#### 模板开发

1.全局过滤器mongo_date_str（格式化mongodb的日期字段）

2.全局函数：

    1）get_page(collection_name, pn=1, size=10, sort_by=None, filter1=None) 分页查询 pn页码 sort_by为tuple类型，目前只支持单字段排序，详情可看模板
    2）get_list(collection_name, sort_by=None, filter1=None, size=None) 列表查询
    3）find_one(collection_name, filter1=None) 获取单条
    4）date_cal(d1, num, is_add=True) 计算日期

#### Todo



1.社交账号登录



