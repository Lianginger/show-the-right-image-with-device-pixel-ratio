# Show the right image with Device Pixel Ratio

隨著手機屏幕分辨率的提高，會發現圖片在手機看起來解析度低的問題，例如：設定一個寬度為 300px 的 img 標籤，顯示一個寬度為 300px 的圖片：

```
<img 
  src="https://i.picsum.photos/id/237/300/300.jpg"
  style="width: 300px;" />
```

會發現在 iPhone 上看起來是模糊的，這是因為 iPhone 其實是用寬度為 600 的設備像素在顯示這張圖，簡單的說：iPhone 等高屏幕分辨率的設備可以顯示更高清的圖片。

[srcset](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) 屬性可以設定不同設備像素比顯示不同的圖片
```
 <img 
  srcset="https://i.picsum.photos/id/237/300/300.jpg 1x,
          https://i.picsum.photos/id/237/450/450.jpg 1.5x,
          https://i.picsum.photos/id/237/600/600.jpg 2x" 
  style="width: 300px;" />
```


在 Chrome 瀏覽器上可以按住 Ctrl + 滑動滾輪的方式，縮放顯示大小來調整設備像素比( window.devicePixelRatio )做測試。

![devicePixelRatio1](https://github.com/Lianginger/show-the-right-image-with-device-pixel-ratio/blob/master/devicePixelRatio100.png)  
在設備像素比為 1 的情況下，3 張圖看起來一樣

![devicePixelRatio1.25](https://github.com/Lianginger/show-the-right-image-with-device-pixel-ratio/blob/master/devicePixelRatio125.png)  
在設備像素比為 1.25 的情況下，左邊第一張圖看起來解析度較低