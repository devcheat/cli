**curl**
===

`curl` is an incredibly powerful command-line tool used for transferring data with URLs. It supports a wide variety of protocols and options, making it useful for APIs, file downloads, authentication, and more.

Here are examples showcasing what `curl` can do:

## **GET Request**
```sh
curl -X GET "https://example.com/api/resource"
```

### GET with Parameter
```sh
curl -X GET "https://example.com/api/resource" 
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" 
     -H "Content-Type: application/json"
     -H "Custom-Header: CustomValue"
```


### Get Request with NTLM
```sh
curl --ntlm -u "username:password" 
-X GET "https://example.com/api/resource" 
-H "Content-Type: application/json"
```

### Get request with OAuth2
```sh
curl -X GET "https://example.com/api/resource" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```


## **POST Request**
```sh
curl -d "option=value&something=anothervalue" -X POST https://example.com
```

### POST Request with JSON Data
```sh
curl -X POST "https://example.com/api/resource" \
     -H "Content-Type: application/json" \
     -d '{"key": "value"}'
```

### Post request with NTLM
```sh
curl --ntlm -u "username:password" -X POST "https://example.com/api/resource" \
     -H "Content-Type: application/json" \
     -d '{"key": "value"}'

```

### Post with OAuth2
```sh
curl -X POST "https://example.com/api/resource" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{"key": "value"}'
```


## **PUT Request**
```sh
curl -X PUT "https://example.com/api/resource" \
     -H "Content-Type: application/json" \
     -d '{"key": "new value"}'
```

### PUT Request with NTLM
```sh
curl --ntlm -u "username:password" -X PUT "https://example.com/api/resource" \
     -H "Content-Type: application/json" \
     -d '{"key": "new value"}'
```

### Put with OAuth2.0
```sh
curl -X PUT "https://example.com/api/resource" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{"key": "new value"}'
```



## **DELETE Request**
```sh
curl -X DELETE "https://example.com/api/resource"
```

---

## **File Downloads & Uploads**
#### Download a File
```sh
curl -O https://example.com/file.zip
```

#### Download a File with a Custom Name
```sh
curl -o myfile.zip https://example.com/file.zip
```

#### Upload a File
```sh
curl -X POST "https://example.com/upload" \
     -H "Content-Type: multipart/form-data" \
     -F "file=@/path/to/file.txt"
```

---

##  **Authentication**
### Basic Authentication
```sh
curl -u "username:password" -X GET "https://example.com/api/protected"
```

### Bearer Token (OAuth2)
```sh
curl -X GET "https://example.com/api/resource" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

### **NTLM Authentication**
```sh
curl --ntlm -u "username:password" -X GET "https://example.com/api/resource"
```

---

## **Handling Headers**
### Custom Headers
```sh
curl -X GET "https://example.com/api/resource" \
     -H "Custom-Header: CustomValue"
```

### Setting User-Agent
```sh
curl -X GET "https://example.com/api/resource" \
     -H "User-Agent: MyCustomAgent"
```

---

## **Handling Cookies**
### Save Cookies
```sh
curl -c cookies.txt -X GET "https://example.com"
```

### Send Saved Cookies
```sh
curl -b cookies.txt -X GET "https://example.com"
```

---

## **Networking & Debugging**
### Follow Redirects
```sh
curl -L "https://example.com"
```

### Check Response Headers
```sh
curl -I "https://example.com"
```

### Verbose Mode (Debugging)
```sh
curl -v "https://example.com"
```

---

## **FTP and SFTP**
### Download a File from FTP
```sh
curl -u "username:password" -O ftp://example.com/file.txt
```

### Upload a File to FTP
```sh
curl -T file.txt -u "username:password" ftp://example.com/upload/
```

---

