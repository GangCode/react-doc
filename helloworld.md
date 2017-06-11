
# React 基本用法
### app.js

    import React from 'react';
    import {render} from 'react-dom';
    
    let html = (<h1>Hello world</h1>);
    render(html,'main');

### index.html【展示核心内容】

    <div id="main"></div>
    <script src="app.js"></script>
