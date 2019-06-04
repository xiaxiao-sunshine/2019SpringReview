# Chapter11 散列与索引

## 11.1 基本概念 <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="搜索码(search key)"/>

* 两种基本的索引类型
  * 顺序索引
  * 散列索引
* 对每种索引技术的评价基于
  * 访问类型(access type)
  * 访问时间(access time)
  * 插入时间(insertion time)
  * 删除时间(deletion time)
  * 空间开销(space overhead)

## 11.2 顺序索引 <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="聚集索引(clustering index)"/> <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="主索引(primary index)"/> <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="非聚集索引(nonclustering index)"/> <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="辅助索引(secondary index)"/> <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="索引顺序文件(index-sequential file)"/>

### 11.2.1 稠密索引和稀疏索引 <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="索引项(index entry)"/>
* 稠密索引(dense index)
* 稀疏索引(sparse index)

&emsp;&emsp;辅助索引必须是稠密索引

&emsp;&emsp;聚集索引可以是稠密索引，也可以是稀疏索引

&emsp;&emsp;稀疏索引必须是聚集索引

### &emsp;11.2.2 多级索引

### &emsp;11.2.3 索引的更新

### &emsp;11.2.4 辅助索引

### &emsp;11.2.5 多码的索引 <input type="button" style="border-width:0;background:#9400D3;padding:4px;border-radius:4px" value="复合搜索码(composite search key)"/>

## 11.3 B+ 树索引文件