## TODO
```dataviewjs
    dv.table(["TODO","地址"],dv.pages('"1-个人文档"').file.tasks.where(t => !t.completed).map(b=>["- [ ] "+b.text,b.link]))
```

## Already Done
```dataviewjs
  dv.table(["TODO","地址","Link"],dv.pages('"1-个人文档"').file.tasks.where(t => t.completed).map(b=>["- [x] "+b.text,b.path,b.link]))
```
