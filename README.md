# 日记

给洲洲的个人日记站。内容由助手指令写入，站点自动部署。

## 怎么加一篇

编辑 `data/entries.json`，在 `entries` 数组开头插入：

```json
{
  "date": "2026-11-02",
  "title": "标题",
  "tags": ["随笔", "复盘"],
  "body": "正文，支持 **加粗**、- 列表、> 引用、![图注](images/xx.jpg)",
  "images": [
    { "src": "images/2026-11-02-1.jpg", "caption": "图注" }
  ]
}
```

图片放 `images/` 目录，文件名用 `日期-序号.jpg`。

## 发布

```bash
git add -A && git commit -m "diary: 2026-11-02" && git push
```

Pages 自动重新构建，约 30 秒生效。

## 账本

`data/expenses.json` 结构：

```json
{
  "budget": 1500,
  "items": [
    { "id": "20261104-1", "date": "2026-11-04", "amount": 12, "cat": "餐饮", "note": "橙 C 美式" }
  ]
}
```

分类建议：餐饮 / 交通 / 画材 / 学习 / 日用 / 娱乐 / 其他
