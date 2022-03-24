# postJsonServer
文章假資料

## Json Server 使用方法 

1. npm install 
2. json-server db.json -m ./node_modules/json-server-auth -r routes.json
3. http://localhost:3000/ 頁面有出現即成功

## API 使用
可用 postman(https://www.postman.com/) 先做測試

註冊 
POST /register
{
  "email": "",
  "password": ""
}

回傳 201 為成功

---------- 

登入
POST /login
```
{
  "email": "",
  "password": ""
}
```
回傳 token 

-------------

取得文章
GET /posts
```
{
  Authorization: Bearer xxxxxxxxxxx
}
```

回傳 
```
{
      "id": 1,
      "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
      "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
    }
```
取得評論
GET /comments
```
{
  Authorization: Bearer xxxxxxxxxxx
}
```
回傳 
```
{
      "postId": 1,
      "authorId": 1,
      "id": 1,
      "body": "laudantium enim quasi est quidem magnam voluptate ipsam eos\ntempora quo necessitatibus\ndolor quam autem quasi\nreiciendis et nam sapiente accusantium"
    },
``` 
 
取得使用者
GET /author
```
{
  Authorization: Bearer xxxxxxxxxxx
}
```

回傳 
```
{
      "id": 1,
      "name": "Author1"
    },
```

