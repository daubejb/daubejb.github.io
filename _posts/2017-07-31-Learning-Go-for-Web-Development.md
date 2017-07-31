# General Notes while Taking the Course Learning Go for Web Development
Course by Larry Price on Lynda.com

## Notes

1. **Install Go on Fedora**

```bash
sudo dnf install golang
```

2. **Configure go path**
```bash
mkdir -p $HOME/go
echo 'export GOPATH=$HOME/go' >> $HOME/.bashrc
source $HOME/.bashrc
```

3. **Check that GOPATH is set right**
```bash
go env GOPATH
```
    - this should yield /home/user/go

4. **Make project folder**
```bash
cd go
mkdir project-name
cd projcet-name
```

5. **Create main package**
```bash
vim main.go
````

```go
package main

func () {
    fmt.Println("Hello, world")
}
```
6.  Make directory "templates" and put in file named index.html
7. **Make sqlite3 dev database**
```bash
sqlite3 dev.db
```

8. The Go sql package relies on us selecting a driver
```bash
go get github.com/mattn/go-sqlite3
```
9.  
