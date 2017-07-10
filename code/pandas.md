把一列数据分割为两列

```python
depth_data['chr'], depth_data['pos'] = zip(*depth_data.Locus.str.split(':',1).tolist())

```
