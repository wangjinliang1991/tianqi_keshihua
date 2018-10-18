# 中国天气网爬虫，练习BeautifulSoup，数据可视化

## 爬取注意
1. response得到的也是有乱码。不能直接response.text
2. table的前两个tr不需要，需要过滤
3. stripped_strings得到的是生成器，获取标签下所有子孙节点的文本信息，需要list
4. 问题：东北的时候不一样，第一个city为黑龙江，稍微修改下，取下标，index为0的话取第二个肯定是城市，
其余的还是依旧
5. 问题： 港澳台的不行，table标签少了</table>导致解析出错，需要用html5lib来解析，容错率高
6. 可视化，按最低气温从小到大排序，新建个ALL_DATA,将最低气温变为int整型
7. 需要安装pyecharts chart.render渲染
8. 抛出异常ModuleNotFoundError: No module named 'pyecharts_snapshot'需要安装pyecharts_snapshot