<?php

/* 
 +--------------------------------------------------------------------+
 |  file:       url_names.php                  version:  2012-05-01   |
 |  by:         Jan Zumwalt - NeatInfo.com                            |
 |  copyright:  GNU GENERAL PUBLIC LICENSE                            |
 |              <a href="http://www.gnu.org/copyleft/gpl.html">http://www.gnu.org/copyleft/gpl.html</a>                  |
 |                                                                    |
 |  purpose:    User supplies web name, program adds prefix and       |
 |              suffix words from array list.                         |
 +--------------------------------------------------------------------+  */
       
  // make things pretty using dark theme     
  echo"
  <head>
    <style>
      body {
        font-size        : 12 pt;
        font-family      : arial;
        color            : #ffb;   /* yellow font color */
        background-color : #123;   /* dark navy bk ground */     
        line-height      : 12pt;
        margin           : 75px;  
      }
    </style>
  </head>
  <body>
  ";
  
  
    // list of prefix words to be added to beginning of URL name
      $prefix  = array(
        "Cool",
        "Fast",
        "Fire",
        "Fry",
        "Hot",
        "Maxi",
        "Quick",
        "Sugar",
        "Super",
        "Sweet",
        "Web",
        "X",
        "Xtra"
      );

    // list of suffix words to be added to end of URL name    
      $suffix = array(   
        "Dog",
        "Hut",
        "Kid",
        "Kit",
        "Man",
        "Power",
        "Pro",
        "Shop",
        "Shot",
        "Store",
        "Wiz",
        "World"
      );
    
  // process form, show prefix and suffix word combinations
  if (isset($_GET['name']) && $_GET['name'] != "") {
  
    $urlname = ucfirst($_GET['name']); // first letter of "name" to uppercase, test -> Test 
    ini_set('max_execution_time', 300);  // (5min) over ride default 30sec timeout error
    
    /* +----------------------------------+
       |          process PREFIX          |
       +----------------------------------+  */
    echo "<br><span style='color:#e33;'><h1>Prefix</h1></span>"; // word list title
    echo "<table>";   
    
    foreach($prefix as $item) {  // add each prefix and show

      echo "<tr><td>" .  $item . $urlname . "</td>";


      
      echo "</tr>";
      
    }   // end of each prefix

    echo "</table>";

    /* +----------------------------------+
       |          process SUFFIX          |
       +----------------------------------+  */    
    echo "<br><span style='color:#e33;'><h1>Suffix</h1></span>"; // word list title 
    echo "<table>";
    
    foreach($suffix as $item) {  // add each prefix and show
      
      echo "<tr><td>" . $urlname . $item . "</td>";


      
      echo "</tr>";
      
    }   // end of each suffix

    echo "</table>";
    echo "<br><span style='color:#6fa;'>Green = ...</span><br>";

  }     // end of process form  
  
// +--------------------   show input form   ---------------------+
  echo "
  <form name='inputform' action=' " . $_SERVER['PHP_SELF'] . " ' method=\"get\">
    URL Name: <input type='text' width='100' maxlength='100' name='name' />
    <input type='submit' value='Submit' />
    <INPUT type='reset' />
    <br><br><b><span style='color:#e33;'>Be patient, this may take several minutes!</span></b>
  </form> 
  ";?>
