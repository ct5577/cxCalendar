#jQuert.cxCalendar

cxCalendar 是基于 jQuery 的日期选择器插件

**版本：**

* jQuery v1.4.4+
* jQuery cxCalendar v1.0

文档：http://code.ciaoca.com/jquery/cxcalendar/

示例：http://code.ciaoca.com/jquery/cxcalendar/demo/

##【options 参数说明】

<table>
    <tr>
        <th width="80">名称</th>
        <th width="100">默认值</th>
        <th>说明</th>
    </tr>
    <tr>
        <td>begin_year</td>
        <td>1950</td>
        <td>起始年份</td>
    </tr>
    <tr>
        <td>end_year</td>
        <td>2030</td>
        <td>结束年份</td>
    </tr>
    <tr>
        <td>date</td>
        <td>new Date()</td>
        <td>
            <p>默认日期。默认使用 javascript 获取当前日期，自定义需使用字符串。日期格式和 type 相同。</p>
            <p>※ input 中的 value 值优先级要高级此值。</p>
        </td>
    </tr>
    <tr>
        <td>type</td>
        <td>"yyyy-mm-dd"</td>
        <td>日期格式。可设置为："yyyy-mm-dd" | "yyyy-m-d"</td>
    </tr>
    <tr>
        <td>hyphen</td>
        <td>"-"</td>
        <td>日期连接符。可设置为："-" | "/" | "."</td>
    </tr>
    <tr>
        <td>wday</td>
        <td>0</td>
        <td>周第一天。可设置为：0-6 之间的数字。
            <p>0=星期日</p>
            <p>1=星期一</p>
            <p>2=星期二</p>
            <p>3=星期三</p>
            <p>4=星期四</p>
            <p>5=星期五</p>
            <p>6=星期六</p>
        </td>
    </tr>
</table>

##【language 语言配置说明】
<table>
    <tr>
        <th width="80">名称</th>
        <th width="400">默认值</th>
        <th>说明</th>
    </tr>
    <tr>
        <td>year</td>
        <td>"年"</td>
        <td></td>
    </tr>
    <tr>
        <td>month</td>
        <td>"月"</td>
        <td></td>
    </tr>
    <tr>
        <td>month_list</td>
        <td>["1","2","3","4","5","6","7","8","9","10","11","12"]</td>
        <td>月份名称。</td>
    </tr>
    <tr>
        <td>week_list</td>
        <td>["日","一","二","三","四","五","六"]</td>
        <td>星期名称。从星期日开始排序</td>
    </tr>
</table>

##【使用方法】

###载入 CSS 文件
```html
<link rel="stylesheet" href="css/jquery.cxcalendar.css">
```

###载入 JavaScript 文件
```html
<script src="js/jquery.js"></script>
<script src="js/jquery.cxcalendar.js"></script>
```

###调用 cxCalendar
```javascript
// 直接调用
$("#element_id").cxCalendar()

// 自定义参数调用
$("#element_id").cxCalendar({
    begin_year:1950,
    end_year:2030,
    date:"1988/1/31",
    type:"yyyy-mm-dd",
    hyphen:"-",
    wday:0
});

// 设置全局默认值，需在引入 <script src="js/jquery.cxselect.js"></script> 之后，调用之前设置
$.cxCalendar.defaults.begin_year=1970;
$.cxCalendar.language={
    year:"",
    month:"",
    month_list:["JAN","FEB","MAR","APR","MAY","JUN","JUL","AUG","SEP","OCT","NOV","DEC"],
    week_list:["Sun","Mon","Tur","Wed","Thu","Fri","Sat"]
};
```