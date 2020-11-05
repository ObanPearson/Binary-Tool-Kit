<div class="searchbox">
  <form method="get" action="http://www.google.com/">
    <input id="searchinput" type="text" placeholder="Search On googLe..." name="q" value="" /> 
    <input type="hidden" name="q1" value="site:{{site.production_url}}" />
  </form>
</div>
.searchbox {
  float:right;
  width: 50%;
  padding: 3px;
  border:0;
  outline: none;
  vertical-align: bottom;
}

#searchinput {
  width:100%;
}
 
