# Less

- ###  变量（Variables）

  - 使用**@变量名**声明变量

  - ```less
    @width: 10px;
    @height: @width + 10px;
    
    #header {
        width: @width;
        height: @height;
    }
    
    // 以上代码编译为：
    
    #header {
        width: 10px;
        height:20px;
    }
    ```

    

- ### 混合（Mixins）

  - 含义：将一组样式规则集以函数的方式混入另外的样式集中

  - ```less
    .bordered {
      border-top: dotted 1px black;
      border-bottom: solid 2px black;
    }
    
    要将上面的样式集用到几个不同的样式中，可以使用“混合的方法”
    
    #menu {
        color: #000000;
        //以函数的方式嵌入
        .bordered();
    }
    
    .mean a {
        background-color: red;
        #border();
    }
    ```

    

- ### 嵌套（Nesting）

  - 可以依据HTML的dom树结构来写css代码，更加的便捷

  - ```less
    #header {
        color: red;
        .login_form {
            height: 100px;
            width: 100px;
        }
        .admin_container {
            height: 100px;
            width: 100%;
            #item {
                color: red;
            }
        }
    }
    ```

    

  - ```less
    .clearfix {
        display: flex;
        zoom: 1;
        
    //&表示当前选择器的父级选择器（下面的表示伪元素）   
        &:after {
            content: " ";
        	display: block;
        	font-size: 0;
        	height: 0;
        	clear: both;
        	visibility: hidden;
        }
    }
    ```

​            