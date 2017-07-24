+++
# Recent Publications widget.
# This widget displays recent publications from `content/publication/`.

date = "2016-04-20T00:00:00"
draft = false

title = "Skills"
subtitle = ""
widget = "publications"

# Order that this section will appear in.
weight = 20

# Number of publications to list.
count = 10

# Show publication details (such as abstract)? (true/false)
detailed_list = false

+++


<style scoped>
body { background: #E9E5E2;margin:2%; }

#SkillBox {
    font-size: 20px;
    font-family: 'Indie Flower', cursive;
    width: 95%;
    height: auto;
    margin: 40px auto;
    background-color: #fff;
    //border: 1px solid #cdcdcd;
    padding: 10px;
    border-radius:20px;
    -o-border-radius:20px;
    -webkit-border-radius:20px;
    -ms-border-radius:20px;
    -moz-border-radius:20px;
}
#SkillBox img {
    width: 20%;
    height: 10%;
    margin: auto 35%;
    padding: 10px;
}
.SkillBar {
    width: 90%;
    height: 50px;
    position: relative;
    background: rgba(17, 17, 17, .3);
    margin: 20px auto;
}
#Skill-HTML {
    width: 75%;
    animation: Animate-HTML 4s;
    -webkit-animation: Animate-HTML 4s;
    -moz-animation: Animate-HTML 4s;
    -o-animation: Animate-HTML 4s;
    height: 50px;
    position: absolute;
    background-color: #ea8564;
}
@keyframes Animate-HTML {
    from {
    width: 10px;
}
to {
    width: 100%}
}@-webkit-keyframes Animate-HTML {
    from {
    width: 10px;
}
to {
    width: 100%}
}@-moz-keyframes Animate-HTML {
    from {
    width: 10px;
}
to {
    width: 100%}
}@-o-keyframes Animate-HTML {
    from {
    width: 10px;
}
to {
    width: 100%}
}#Skill-CSS {
    animation: Animate-CSS 5s;
    -webkit-animation: Animate-CSS 5s;
    -moz-animation: Animate-CSS 5s;
    -o-animation: Animate-CSS 5s;
    width: 70%;
    height: 50px;
    position: absolute;
    background-color: #55a69f;
}
@keyframes Animate-CSS {
    from {
    width: 10px;
}
to {
    width: 70%}
}@-webkit-keyframes Animate-CSS {
    from {
    width: 10px;
}
to {
    width: 70%}
}@-moz-keyframes Animate-CSS {
    from {
    width: 10px;
}
to {
    width: 70%}
}@-o-keyframes Animate-CSS {
    from {
    width: 10px;
}
to {
    width: 70%}
}#Skill-jQuery {
    animation: Animate-jQuery 5s;
    -webkit-animation: Animate-jQuery 5s;
    -moz-animation: Animate-jQuery 5s;
    -o-animation: Animate-jQuery 5s;
    width: 40%;
    height: 50px;
    position: absolute;
    background-color: #99856d;
}
@keyframes Animate-jQuery {
    from {
    width: 10px;
}
to {
    width: 40%}
}@-webkit-keyframes Animate-jQuery {
    from {
    width: 10px;
}
to {
    width: 40%}
}@-moz-keyframes Animate-jQuery {
    from {
    width: 10px;
}
to {
    width: 40%}
}@-o-keyframes Animate-jQuery {
    from {
    width: 10px;
}
to {
    width: 40%}
}#Skill-JS {
    animation: Animate-JS 4s;
    -webkit-animation: Animate-JS 4s;
    -moz-animation: Animate-JS 4s;
    -o-animation: Animate-JS 4s;
    width: 70%;
    height: 50px;
    position: absolute;
    background-color: #c44e45;
}
@keyframes Animate-JS {
    from {
    width: 10px;
}
to {
    width: 65%}
}@-webkit-keyframes Animate-JS {
    from {
    width: 10px;
}
to {
    width: 65%}
}@-moz-keyframes Animate-JS {
    from {
    width: 10px;
}
to {
    width: 65%}
}@-o-keyframes Animate-JS {
    from {
    width: 10px;
}
to {
    width: 65%}
}#Skill-XML {
    animation: Animate-XML 4s;
    -webkit-animation: Animate-XML 4s;
    -moz-animation: Animate-XML 4s;
    -o-animation: Animate-XML 4s;
    width: 65%;
    height: 50px;
    position: absolute;
    background-color: #5aa669;
}
@keyframes Animate-XML {
    from {
    width: 10px;
}
to {
    width: 40%}
}@-webkit-keyframes Animate-XML {
    from {
    width: 10px;
}
to {
    width: 40%}
}@-moz-keyframes Animate-XML {
    from {
    width: 10px;
}
to {
    width: 40%}
}@-o-keyframes Animate-XML {
    from {
    width: 10px;
}
to {
    width: 40%}
}#Skill-C {
    animation: Animate-C 4s;
    -webkit-animation: Animate-C 4s;
    -moz-animation: Animate-C 4s;
    -o-animation: Animate-C 4s;
    width: 65%;
    height: 50px;
    position: absolute;
    background-color: #970cc1;
}
@keyframes Animate-C {
    from {
    width: 10px;
}
to {
    width: 30%}
}@-webkit-keyframes Animate-C {
    from {
    width: 10px;
}
to {
    width: 30%}
}@-moz-keyframes Animate-C {
    from {
    width: 10px;
}
to {
    width: 30%}
}@-o-keyframes Animate-C {
    from {
    width: 10px;
}
to {
    width: 30%}
}#Skill-JAVA {
    animation: Animate-JAVA 4s;
    -webkit-animation: Animate-JAVA 4s;
    -moz-animation: Animate-JAVA 4s;
    -o-animation: Animate-JAVA 4s;
    width: 95%;
    height: 50px;
    position: absolute;
    background-color: #8e930c;
}
@keyframes Animate-JAVA {
    from {
    width: 10px;
}
to {
    width: 25%}
}@-webkit-keyframes Animate-JAVA {
    from {
    width: 10px;
}
to {
    width: 25%}
}@-moz-keyframes Animate-JAVA {
    from {
    width: 10px;
}
to {
    width: 25%}
}@-o-keyframes Animate-JAVA {
    from {
    width: 10px;
}
to {
    width: 25%}
}#Skill-NOSQL {
    animation: Animate-PHP 4s;
    -webkit-animation: Animate-PHP 4s;
    -moz-animation: Animate-PHP 4s;
    -o-animation: Animate-PHP 4s;
    width: 75%;
    height: 50px;
    position: absolute;
    background-color: #5A69A6;
}
@keyframes Animate-PHP {
    from {
    width: 10px;
}
to {
    width: 50%}
}@-webkit-keyframes Animate-PHP {
    from {
    width: 10px;
}
to {
    width: 50%}
}@-moz-keyframes Animate-PHP {
    from {
    width: 10px;
}
to {
    width: 50%}
}@-o-keyframes Animate-PHP {
    from {
    width: 10px;
}
to {
    width: 50%}
}#Skill-SQL {
    animation: Animate-SQL 4s;
    -webkit-animation: Animate-SQL 4s;
    -moz-animation: Animate-SQL 4s;
    -o-animation: Animate-SQL 4s;
    width: 85%;
    height: 50px;
    position: absolute;
    background-color: #23b1db;
}
@keyframes Animate-SQL {
    from {
    width: 10px;
}
to {
    width: 80%}
}@-webkit-keyframes Animate-SQL {
    from {
    width: 10px;
}
to {
    width: 80%}
}@-moz-keyframes Animate-SQL {
    from {
    width: 10px;
}
to {
    width: 80%}
}@-o-keyframes Animate-SQL {
    from {
    width: 10px;
}
to {
    width: 80%}
}#Skill-ANGULAR {
    animation: Animate-VBNET 4s;
    -webkit-animation: Animate-VBNET 4s;
    -moz-animation: Animate-VBNET 4s;
    -o-animation: Animate-VBNET 4s;
    width: 85%;
    height: 50px;
    position: absolute;
    background-color: #f8a51e;
}
@keyframes Animate-VBNET {
    from {
    width: 10px;
}
to {
    width: 35%}
}@-webkit-keyframes Animate-VBNET {
    from {
    width: 10px;
}
to {
    width: 35%}
}@-moz-keyframes Animate-VBNET {
    from {
    width: 10px;
}
to {
    width: 35%}
}@-o-keyframes Animate-VBNET {
    from {
    width: 10px;
}
to {
    width: 35%}
}.Skill-Area {
    z-index: 1;
    float: left;
    //position: absolute;
    margin-top: 15px;
    margin-left: 15px;
    text-shadow: none;
    color: #fff;
    //font-family: Lato-Regular, sans-serif;
    font-size: 18px;
}
.PercentText {
    z-index: 3;
    position: relative;
    padding-right: 15px;
    margin-top: 15px;
    float: right;
    text-shadow: none;
    color: #fff;
    //font-family: Lato-Regular, sans-serif;
    font-size: 18px;
}

</style>
<body>
<center>
<div id="SkillBox">
        <center><p>My Skills</p></center>
  <div class="SkillBar">
    <div id="Skill-HTML">
      <span class="Skill-Area ">HTML/HTML5</span>
      <span class="PercentText ">75%</span>
    </div>
  </div>

  <div class="SkillBar">
  <div id="Skill-JAVA">
    <span class="Skill-Area ">JAVA </span>
    <span class="PercentText ">95%</span>
  </div>
</div>

  <div class="SkillBar">
  <div id="Skill-NOSQL">
    <span class="Skill-Area ">NOSQL(MongoDB) </span>
    <span class="PercentText ">75%</span>
  </div>
</div>

  <div class="SkillBar">
  <div id="Skill-SQL">
    <span class="Skill-Area ">SQL </span>
    <span class="PercentText ">85%</span>
  </div>
</div>

  <div class="SkillBar">
  <div id="Skill-ANGULAR">
    <span class="Skill-Area ">AngularJS</span>
    <span class="PercentText ">85%</span>
  </div>
</div>

  <div class="SkillBar">
    <div id="Skill-CSS">
      <span class="Skill-Area ">CSS/CSS3</span>
      <span class="PercentText ">70%</span>
    </div>
  </div>

  <div class="SkillBar">
  <div id="Skill-C">
    <span class="Skill-Area ">C</span>
    <span class="PercentText ">65%</span>
  </div>
</div>

  <div class="SkillBar">
    <div id="Skill-jQuery">
      <span class="Skill-Area ">jQuery</span>
      <span class="PercentText ">40%</span>
    </div>
  </div>

  <div class="SkillBar">
    <div id="Skill-JS">
      <span class="Skill-Area ">Javascript</span>
      <span class="PercentText ">70%</span>
    </div>
  </div>

  <div class="SkillBar">
    <div id="Skill-XML">
      <span class="Skill-Area ">XML </span>
      <span class="PercentText ">65%</span>
    </div>
  </div>

</div>
</center>
</body>
