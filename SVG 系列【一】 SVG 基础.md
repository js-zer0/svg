##### SVG 可伸缩适量图形（Scalable Vector Graphics）。
##### SVG 使用 XML 格式定义图像。

## SVG 的优势

- 可被非常多的工具读取和修改
- 与 JPEG 和 GIF 图像比起来，尺寸更小，且可压缩性更强
- 可在图像质量不下降的情况下被放大
- 图像可在任何的分辨率下被高质量的打印
- 图像中的文本是可选的，同时也是可搜索的
- SVG 文件是纯粹的 XML

## 查看 SVG 文件

IE 9+、chrome、firefox、opera、safari都支持 svg
IE 8 和早期版本需要一个插件

## SVG 文件组成
    <?xml version="1.0" standalone="no"?>
    // XML 声明，standalone 属性表示此文件是独立的，还是含有对外部文件的引用，
    // 在这里 standalone=“no” 表示意味着 svg 文档会引入一个外部文件，这里是 DTD 文件
    <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
    "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
    // 引入的外部文件 svg dtd，位于 W3C，包含所有允许的 svg 元素
    <svg xmlns="http://www.w3.org/2000/svg" version="1.1">
         <circle cx="100" cy="50" r="40" stroke=“black" stroke-width="2" fill="red" />
    </svg>
    // svg 为根元素，xmlns 表示 svg 命名空间，version 表示 svg 版本
    
#### 注意，所有的开启标签必须有关闭标签。

## 在 HMTL 中使用 SVG 

#### 1. 直接在 html 中嵌入 svg 代码
     直接将 svg 的代码写在 body 中
     注意，opera 不能直接嵌入 svg。

#### 2. 链接到 svg 文件
    
    <a href="circle1.svg">View SVG file</a>