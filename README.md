# 多种省略号解决情况(css,js)

多种省略号方案

# css:

.css{ //一行

    overflow:hidden;
    
    text-overflow:ellipsis;//超出部分省略号表示
    
    white-space:no-wrap

}

.css1 { //伪类
    
    position:relative;
    
    line-height:20px;
    
    max-height:40px;
    
    over-flow:hidden
    
}
.css1::after {

    position:absolute;
    
    content:'...';
    
    bottom:0;
    
    right:0;
    
    padding-left: 40px;
    
    background: -webkit-linear-gradient(left, transparent, #fff 55%); 

}

# js:

  function join...(val=''){
    
    let str = val.split(/(?<=[\u4e00-\u9fa5])|(?<=\w*?\b)/g)
    
    str = val.length > 12 ? str.join() + '...':str
    
    return str
         
  }
