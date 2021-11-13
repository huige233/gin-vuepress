# gin-vuepress

## the test use

## test use name:admin

## test use password:123456

## How to use the gin-vue

```
- node version > v8.6.0
- golang version >= v1.14
- IDE recommendation: Goland
- initialization project: different versions of the database are not initialized. See synonyms at initialization https://www.gin-vue-admin.com/docs/first
- Replace the Qiniuyun public key, private key, warehouse name and default url address in the project to avoid data confusion in the test file.
```

### 2.1 server project

use `Goland` And other editing tools，open server catalogue，You can't open it. `gin-vue-admin` root directory

```bash
# clone the project
git clone https://github.com/flipped-aurora/gin-vue-admin.git

# open server catalogue
cd server

# use go mod And install the go dependency package
go generate

# Compile 
go build -o server main.go (windows the compile command is go build -o server.exe main.go )

# Run binary
./server (windows The run command is server.exe)
```

### 2.1 web project

```bash
# enter the project directory
cd web

# install dependency
npm install

# develop
npm run serve
```

### 2.2 Server

```bash
# using go.mod

# install go modules
go list (go mod tidy)

# build the server
go build
```

### 2.3 API docs auto-generation using swagger

#### 2.3.1 install swagger 

##### (1) Using VPN or outside mainland China

````
go get -u github.com/swaggo/swag/cmd/swag
````

## project layout


```
    ├── server
        ├── api             (api entrance)
        │   └── v1          (v1 version interface)
        ├── config          (configuration package)
        ├── core            (core document)
        ├── docs            (swagger document directory)
        ├── global          (global object)                    
        ├── initialize      (initialization)                        
        │   └── internal    (initialize internal function)                            
        ├── middleware      (middleware layer)                        
        ├── model           (model layer)                    
        │   ├── request     (input parameter structure)                        
        │   └── response    (out-of-parameter structure)                            
        ├── packfile        (static file packaging)                        
        ├── resource        (static resource folder)                        
        │   ├── excel       (excel import and export default path)                        
        │   ├── page        (form generator)                        
        │   └── template    (template)                            
        ├── router          (routing layer)                    
        ├── service         (service layer)                    
        ├── source          (source layer)                    
        └── utils           (tool kit)                    
            ├── timer       (timer interface encapsulation)                        
            └── upload      (oss interface encapsulation)  
            
    └─web            （frontend）
        ├─public        （deploy templates）
        └─src           （source code）
            ├─api       （frontend APIs）
            ├─assets	（static files）
            ├─components（components）
            ├─router	（frontend routers）
            ├─store     （vuex state management）
            ├─style     （common styles）
            ├─utils     （frontend common utilitie）
            └─view      （pages）

```
