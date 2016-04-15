# ScanBarCodeViewController
ios自定义一个扫描二维码/条码功能的控制器

##How to use ?
```
ScanBarCodeViewController *scanBarCodeVC = [[ScanBarCodeViewController alloc] init];
    scanBarCodeVC.delegate = self;
    //使用self.view.window.rootViewController进行模态跳转不会导致返回时view偏移的bug
    [self.view.window.rootViewController presentViewController:scanBarCodeVC animated:YES completion:nil];

//实现代理
- (void)scanCallback:(NSString *)dimensionCode
{
	//拿到条码内容
}
```