# 1. GoConvey测试框架

```go
import "github.com/smartystreets/goconvey/convey"

func CheckUrl(url string) bool {
    var urlList = [2]string{"learnku.com", "xdcute.com"}
    for v := range urlList {
        if urlList[v] == url {
            return true
        }
    }
    return false
}

func TestCheckUrl(t *testing.T) {
    convey.Convey("TestCheckTeachUrl", t, func() {
        ok:=CheckUrl("learnku.com")
        convey.So(ok,convey.ShouldBeTrue)
    })
}
```

官方文档:https://github.com/smartystreets/goconvey/wiki/Assertions