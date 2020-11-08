## 学习笔记

### CSSOM

    The CSS Object Model is a set of APIs allowing the manipulation of CSS from JavaScript. It is much like the DOM, but for the CSS rather than the HTML. It allows users to read and modify CSS style dynamically.
    https://developer.mozilla.org/en-US/docs/Web/API/CSS_Object_Model

### proxy

    The Proxy object enables you to create a proxy for another object, which can intercept and redefine fundamental operations for that object.
    https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy

### 拖拽的骨架代码

    ```
    var dragable = document.getElementById('container')
    dragable.addEventListener('mousedown', (event)=>{

        const up = ()=>{
            document.removeEventListener('mouseup', up);
            document.removeEventListener('mousemove', move);
        }
        const move = (event)=>{
            console.log(event)
            dragable.style.transform = `translate(${event.clientX}px, ${event.clientY}px)`
        }
        document.addEventListener('mousemove', move)
        document.addEventListener('mouseup', up)
    })
    ```
