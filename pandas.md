### pandas 多层索引切片
####导入数据

![read_csv](https://gitee.com/frankheee/blog_django/raw/master/2020/8/31/8/53/33.jpg)
```python
def get_df():
	df=pd.read_csv(
		g_new_path,
		encoding=g_encoding,
		index_col=[0,1],
		header=[0,1]
		)
```
####数据示例

![avatar](https://gitee.com/frankheee/blog_django/raw/master/2020/8/29/9/56/22.jpg)
```
df.loc['珠海','白天']
```
![avatar](https://gitee.com/frankheee/blog_django/raw/master/2020/8/29/10/0/12.jpg)
#### 执行过程示意：
![abb](https://gitee.com/frankheee/blog_django/raw/master/2020/8/29/10/16/0.jpg)