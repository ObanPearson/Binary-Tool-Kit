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
 
<!ENTITY % plistObject "(array | data | date | dict | real | integer | string | true | false )" >
<!ELEMENT plist %plistObject;>
<!ATTLIST plist version CDATA "1.0" >

<!-- Collections -->
<!ELEMENT array (%plistObject;)*>
<!ELEMENT dict (key, %plistObject;)*>
<!ELEMENT key (#PCDATA)>

<!--- Primitive types -->
<!ELEMENT string (#PCDATA)>
<!ELEMENT data (#PCDATA)> <!-- Contents interpreted as Base-64 encoded -->
<!ELEMENT date (#PCDATA)> <!-- Contents should conform to a subset of ISO 8601 (in particular, YYYY '-' MM '-' DD 'T' HH ':' MM ':' SS 'Z'.  Smaller units may be omitted with a loss of precision) -->

<!-- Numerical primitives -->
<!ELEMENT true EMPTY>  <!-- Boolean constant true -->
<!ELEMENT false EMPTY> <!-- Boolean constant false -->
<!ELEMENT real (#PCDATA)> <!-- Contents should represent a floating point number matching ("+" | "-")? d+ ("."d*)? ("E" ("+" | "-") d+)? where d is a digit 0-9.  -->
<!ELEMENT integer (#PCDATA)> <!-- Contents should represent a (possibly signed) integer number in base 10 -->
- name: Deploy Flutter web app to github pages
  uses: erickzanardo/flutter-gh-pages@v2

