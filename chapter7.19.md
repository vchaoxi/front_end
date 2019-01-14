# 面向对象

#### 面向过程与面向对象编程

1、面向过程：所有的工作都是现写现用。

2、面向对象：是一种编程思想，许多功能事先已经编写好了，在使用时，只需要关注功能的运用，而不需要这个功能的具体实现过程。

#### javascript对象 
将相关的变量和函数组合成一个整体，这个整体叫做对象，对象中的变量叫做属性，变量中的函数叫做方法。javascript中的对象类似字典。

#### 创建对象的方法 
1、单体

```
<script type="text/javascript">
var Tom = {
    name : 'tom',
    age : 18,
    showname : function(){
        alert('我的名字叫'+this.name);    
    },
    showage : function(){
        alert('我今年'+this.age+'岁');    
    }
}
</script>
```


2、工厂模式

```

<script type="text/javascript">

function Person(name,age,job){
    var o = new Object();
    o.name = name;
    o.age = age;
    o.job = job;
    o.showname = function(){
        alert('我的名字叫'+this.name);    
    };
    o.showage = function(){
        alert('我今年'+this.age+'岁');    
    };
    o.showjob = function(){
        alert('我的工作是'+this.job);    
    };
    return o;
}
var tom = Person('tom',18,'程序员');
tom.showname();

</script>
```

2、构造函数

```
<script type="text/javascript">
    function Person(name,age,job){            
        this.name = name;
        this.age = age;
        this.job = job;
        this.showname = function(){
            alert('我的名字叫'+this.name);    
        };
        this.showage = function(){
            alert('我今年'+this.age+'岁');    
        };
        this.showjob = function(){
            alert('我的工作是'+this.job);    
        };
    }
    var tom = new Person('tom',18,'程序员');
    var jack = new Person('jack',19,'销售');
    alert(tom.showjob==jack.showjob);
</script>
```


3、原型模式

```
<script type="text/javascript">
    function Person(name,age,job){        
        this.name = name;
        this.age = age;
        this.job = job;
    }
    Person.prototype.showname = function(){
        alert('我的名字叫'+this.name);    
    };
    Person.prototype.showage = function(){
        alert('我今年'+this.age+'岁');    
    };
    Person.prototype.showjob = function(){
        alert('我的工作是'+this.job);    
    };
    var tom = new Person('tom',18,'程序员');
    var jack = new Person('jack',19,'销售');
    alert(tom.showjob==jack.showjob);
</script>
```


**4、继承**

```

<script type="text/javascript">

        function fclass(name,age){
            this.name = name;
            this.age = age;
        }
        fclass.prototype.showname = function(){
            alert(this.name);
        }
        fclass.prototype.showage = function(){
            alert(this.age);
        }
        function sclass(name,age,job)
        {
            fclass.call(this,name,age);
            this.job = job;
        }
        sclass.prototype = new fclass();
        sclass.prototype.showjob = function(){
            alert(this.job);
        }
        var tom = new sclass('tom',19,'全栈工程师');
        tom.showname();
        tom.showage();
        tom.showjob();
    </script>
    ```
    