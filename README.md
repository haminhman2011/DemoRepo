# DemoRepo
Menu is an integral part of the website. The construction of a logical menu system and ease of use is not simple, especially websites with multi-level and system complexity. Drop-down menu (drop-down menu) is the first choice for this website
drop-down-menu


To obtain a multi-level menu system as above, you can follow the steps as stars:
1/
Create an HTML menu system:
Often in programming, the system will automatically generate html menu, here is the html simulation for a multi-level menu
<div>
      <ul>
        <li>
            <a href="#">Menu 1</a>
            <ul>
                <li><a href="#">Menu 1 - Lv2</a>
                    <ul>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                    </ul>
                </li>
                <li><a href="#">Menu 1 - Lv2</a>
                    <ul>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                        <li><a href="#">Menu 1 - Lv3</a></li>
                    </ul>
                </li>
                <li><a href="#">Menu 1 - Lv2</a></li>
                <li><a href="#">Menu 1 - Lv2</a></li>
                <li><a href="#">Menu 1 - Lv2</a></li>
            </ul>
        </li>
   </ul>
</div>

2/CSS on menu: 
<style type="text/css">
.menu
{
    width:70%; 
    height:30px; 
    line-height:30px;
    margin:0 auto;
}
.menu li
{
    position:relative;
    display:inline-block;
    width:100%;
}
.menu li ul
{
    position:absolute; 
    display:none;
}
.menu li:hover > ul
{
    display:block;
}
.menu a
{
    display:block; 
    color:#fff;
    background:#606c88;
}
.menu ul ul,
.menu li:hover > a,
.menu a:hover
{
    opacity:.8;
}
/*Level 1*/
.menu > ul > li
{
    float:left;
    width:24%;
}
.menu > ul > li > a
{
    width:94%;
    padding-left:3%; 
    padding-right:3%; 
    text-transform:uppercase; 
    font-weight:bold;
}
/*Level 2*/
.menu > ul > li > ul
{
    position:absolute; 
    top:100%; 
    left:0; 
    width:100%; 
}
.menu > ul > li > ul > li
{
    width:100%;
}
.menu > ul > li > ul > li > a
{
    width:94%;
    padding-left:3%;
    padding-right:3%;
}
/* Level +++ */
.menu ul ul ul
{
    width:100%;
    left:100%;
    top:0;
    background:#a1b1d4;
}
.menu ul ul ul li
{
    width:100%;
}
.menu ul ul ul li a
{
    width:94%;
    padding-left:3%;
    padding-right:3%;
}

</style>


CSS code using% as the unit, so the menu will stretch the width of the website. You can specify the width by a specific set width for the menu.

You can use the demo file to the build menu templates for your website. You can use jQuery to animate the menu becomes smoother, this article guides you to create menus using CSS, so the guide using jQuery effects for menus please see the instructions at another article.
