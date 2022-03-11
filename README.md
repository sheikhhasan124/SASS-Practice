# SASS 

## 1 what is sass?  
1. SASS = syntactically awesome style sheet  
2. it is an extension of css  

## 2 why sass?
1. sass has some extra special features that do not exist in css.  
i. variables  
ii. nested rules,  
iii. mixins, imports,  
iv. inheritance.  
2. To make our code simpler and more maintainable
3. No DRY (we can @extends css rules)

## 3 how does sass work?
1. demo.scss  
## 4 how to add sass to html?
1. install live sass compiler in vscode  
2. create a style folder -> demo.scss-> add some code into it  
3. link rel = 'stylesheet' href='./style.demo.css'


# SASS features
1. Sass variables  
2. Nesting css rules  
3. @import and partials (import file-reset,color etc,DRY)  
4. @mixin and @include (@mixin holds reusable code and we can implement that code using @include)  
5. @extend and inheritance  
6. @if @else if @else  
7. @for  
8. @while  
9. @each    

<hr>

## (c-2)
## sass variables  
sass variable is more simpler than css  
like js (let,const) we can start declaring the variable using $  

### example  
### declaring  
$header-bgcolor: colorName;
$para-fontsize: size;  

### using  
header{
    bacground: $header-bgcolor;  
}  

### using sass variable we can stor  
- string  
- numbers  
- colors  
- booleans  
- lists  
- nulls  

<hr>

## @mixin and @include  
- A mixin -> a group of CSS declarations that can be reuses throughout the style sheet.  

```
@mixin para-style{
    font-size:10px;
    text-align:justify;
}

```
```
#section-me p{
    @include para-style;
}

```
```
@mixin para-style($size, $style) {
    font-size: $size;
    text-align: $style;
    margin: 10px
}

#about p{
    @include para-style(25px, center);
}           
#service p{
    @include para-style(20px, left);
}  

```

<hr>

## extend and inheritense  
```
     <input type="button" class="click-btn" value="click">
       <input type="button" class="reset-btn" value="reset"



.btn{
    border: none;
   padding: 10px;
   font-size: 15px;
   border-radius: 20px;
}
.click-btn{
    @extend .btn;
}
.reset-btn{
    @extend .btn;
}
```