# Laboratorul Nr.1

 În dependenţă de vârstă să se afişeze mesajele, dacă vîrsta este >18
    şi < 60 – “ Mai aveţi mult de lucru” ; dacă vîrsta este >1 şi 18 < –
    “ E devreme să lucraţi” ; dacă vîrsta este >60 – “ E timpul să vă   
    pensionaţi” ; în restu cazurilor se va afişa “ Vârstă necunoscută”.

----------

    <?php
    $virsta = 12;
    
    if ($virsta < 18) echo "E devreme să lucrați";
      else
    if ($virsta > 16 && $virsta < 60) echo "Mai aveţi mult de lucru";
      else
    if ($virsta >= 60) echo "E timpul să vă pensionaţi";
      else echo "Vârstă necunoscută";
    ?>


----------
 Sunt date 2 numere. Să se găsească suma patratelor lor.

    <?php
    $a = 2;
    $b = 6;
    echo "suma patrateleor:" . (($a * $a) + ($b * $b));
    ?>
  
# Laboratorul Nr.2  -  *Tipul tablou*
Elementul maximal din tablou. 

    <?php
    $a = [3, 6, 52, 16, 42, 2, 19];
    $max = $a[0];
    echo "Dintre numerele: ";
    
    for ($i = 0; $i < count($a); $i++) echo $a[$i] . " ";
    
    for ($i = 1; $i < count($a); $i++)
    	{
    	if ($max < $a[$i])
    		{
    		$max = $a[$i];
    		}
    	  else
    		{
    		$max = $max;
    		}
    	}
    
    echo ", Cel mai mare numar este: $max.<br /> <br />";
    ?>
    


----------


Este dat un tablou din numere reale a[0]..a[n-1]. De găsit pozitia primului element care este >100. Celelalte elemente care urmează să se împarta la 100. Să se afişeze tabelul iniţial şi tabelul rezultant.
 

     <?php
    	    $b = [0,1.5,100.1,223,151.4,100.02,56,13];
    		$e = 100;
    		echo"Tabloul initial:<br>";
    		for($i = 0; $i < count($b); $i++) 
    			echo"<tr><td> a[$i] = </td> <td>$b[$i] </td></tr> <br>";
    		for($i = 0; $i < count($b); $i++){
    			if($e < $b[$i]){
    				$e = $b[$i];
    				$poz = $i;
    				break;				
    				}
    		}
    		for($i = $poz + 1; $i < count($b); $i++){
    			$b[$i] = $b[$i] / 100;
    		}
    		echo "<br>Tabloul nou este: <br>";
    		for($i = 0; $i < count($b); $i++) 
    			echo"<tr><td> a[$i] = </td> <td>$b[$i] </td></tr> <br>";
    		echo "<br>";
    	  ?>


----------


Este dat un tablou cu simbolurile S[0]..S[n-1].Sa se afişeze adevar daca în acest tablou simbolul  a  se intilneşte mai des decit simbolul  b şi false în caz contrar.
 

     <?php
    	    $S = ["a","b","c","b","b","d","a","b"];
    		$k1 = 0;
    		$k2 = 0;
    		echo"In tabloul: ";
    		for($i = 0; $i < count($S); $i++) 
    			echo $S[$i]." ";
    		for($i = 0; $i < count($S); $i++){
    			if($S[$i] === "a") $k1++;
    			if($S[$i] === "b") $k2++;
    		}
    		echo " , simbolul a se intilneste mai des decit simbolul b. - ";
    		if($k1 > $k2) echo "Adevar!";
    		 else echo "Fals!";
    		echo "<br><br>";
    	  ?>


----------


Este dat un tablou  a[0]..a[n-1].De găsit in această consecutivitate perechile a[i]..a[i+1] astfel încit a[i]*a[i+1]  să fie divizibil prin 10.

    <?php
    	    $c = [1,5,15,50,42,2,19];
    		$k = 0;
    		echo "Din acest tablou de numere: ";
    	    for($i = 0; $i < count($c); $i++) 
    			echo $c[$i]." ";
    		echo" perechile din elemente consecutive a carui produs se divide cu 10 sunt: <br>";
    		for($i = 0; $i < count($c); $i++){
    			$f1 = $c[$i];
    			if($i != count($c) - 1) $f2 = $c[$i+1];
    			 else $f2 = $c[0];
    			if(($f1 * $f2) % 10 === 0){
    				echo $f1." ".$f2. "<br>";	
    				$k++;
    			}
    		}
    		if($k === 0) echo "Nu sunt asa perechi de elemente in acest tablou.";
    		echo "<br> <br>";
    	  ?>


----------


Este dat un tablou  a[0]..a[n-1]. Să se afişeze toate  elementele de la a[0]..a[4].

    <?php
    	    $a = [1,5,"cuvint",15,"php",2,19];
    	    echo "Primele cinci elemente ale tabloului: <br>";
    	    for($i = 0; $i < count($a); $i++) 
    			echo $a[$i]." ";
    		echo"<br> sunt: <br>";
    		for($i = 0; $i < 5; $i++) 
    			echo $a[$i]." ";
    		echo "<br> <br>";
    	  ?>


----------


Este dat un tablou a[0]..a[n-1].Să se compare toate elementele cu elementul din mijloc a tabloului.

    <?php
    	    $c = [1,5,15,50,42,2,19,79];
    		count($c);
    		echo "Tabloul de elemente: <br>";
    		for($i = 0; $i < count($c); $i++) 
    			echo $c[$i]." ";
    		$m = count($c) / 2;
    		echo "<br> Elementul(ele) din mijlocul tabloului este/sunt: ";
    		if(count($c) % 2 != 0) {
    			$poz1 = $m-0.5;
    			echo $c[$poz1]."<br>";
    		} else{
    			$poz1 = $m;
    			$poz2 = $m-1;
    			echo $c[$poz1]." ".$c[$poz2]."<br>";
    		 }
    		for($i = 0; $i < count($c); $i++){
    			if($i != $poz1)
    				if($c[$i] < $c[$poz1]) echo $c[$i]." < ".$c[$poz1]."<br>";
    			else if($c[$i] > $c[$poz1]) echo $c[$i]." > ".$c[$poz1]."<br>";
    			else if($c[$i] === $c[$poz1]) echo $c[$i]." = ".$c[$poz1]."<br>";
    		}
    		if(isset($poz2)){
    			echo "<br>";
    			for($i = 0; $i < count($c); $i++){
    			if($i != $poz2)
    				if($c[$i] < $c[$poz2]) echo $c[$i]." < ".$c[$poz2]."<br>";
    			else if($c[$i] > $c[$poz2]) echo $c[$i]." > ".$c[$poz2]."<br>";
    			else if($c[$i] === $c[$poz2]) echo $c[$i]." = ".$c[$poz2]."<br>";
    			}
    		}
    		echo "<br> <br>";		 
    	  ?>


----------


Este dat un tablou de caractere si numere. Să se sorteze elementele  numerice si  cele string.

      <?php
    	    $a = [1,5,"cuvint",15,"php",2,19];
    		$k = 0;
    	    echo "Elementele tabloului dat sunt: <br>";
    	    for($i = 0; $i < count($a); $i++) 
    			echo $a[$i]." ";
    		echo "<br> Elementele numerice sunt: <br>";
    		for($i = 0;$i < count($a);$i++){
    			if(is_numeric($a[$i])) {
    				echo $a[$i]." ";
    				$k++;
    			}
    		}
    		if($k === 0) echo "Tabloul nu are elemente numerice.";
    		echo "<br> Elementele string sunt: <br>";
    		for($i = 0; $i < count($a); $i++){
    			if(!is_numeric($a[$i])) {
    				echo $a[$i]." ";
    				$k++;
    			}
    		}
    		if($k === 0) echo "Tabloul nu are elemente string.";
    		echo "<br> <br>";
    	  ?>
    	  8.Se dau doua tablouri diferite. Să se unească aceste tablouri în unul singur.
    
    	  <li> Se dau doua tablouri diferite. 
    	  Sa se unească aceste tablouri in unul singur. <br>
    	  <?php
    	    $a = [1,5,"cuvint",15,"php",2,19];
    		$b = ["hello","emotie",220,"base"];
    		$c = array_merge($a,$b);
    		echo "Tabloul a este: <br>";
    		for($i = 0; $i < count($a); $i++) 
    			echo $a[$i]." ";
    		echo "<br> Tabloul b este: <br>";
    		for($i = 0; $i < count($b); $i++) 
    			echo $b[$i]." ";
    		echo "<br> Tabloul nou este: <br>";
    		for($i = 0; $i < count($c); $i++) 
    			echo $c[$i]." ";
    		echo "<br> <br> ";
    	  ?>
    	  


----------


Este dat un tablou a[0]..a[n-1] numere positive si negative. Să se afişeze suma şi produsul acestor numere.

    <?php
    	    $a = [-32,15,29,45,-69.15,114.0002];
    		$sum1 = 0; $sum2 = 0;
    		$prod1 = 1; $prod2 = 1;
    		echo "Tabloul dat este: <br>";
    		for($i = 0; $i < count($a); $i++) 
    			echo $a[$i]." ";
    		for($i = 0; $i < count($a); $i++){
    			if($a[$i] > 0){
    				$sum1 =+ $a[$i];
    				$prod1 = $prod1 * $a[$i];
    			}
    			else{
    				$sum2 =+ $a[$i];
    				$prod2 = $prod2 * $a[$i];
    			}
    		}
    	    echo "<br> Numerele pozitive: <br> Suma = ".$sum1." , Produsul = ".$prod1."<br>";
    		echo "Numerele negative: <br> Suma = ".$sum2." , Produsul = ".$prod2;
    	  ?>

# Laboratorul Nr.3  -  *Crearea formularelor*
Creati un formular pentru alegerea cursurilor obtionale dorite:

 1. Nume,Prenume
 2. Facultatea
 3. Specialitatea
 4. Grupa
 5. Cursul optional: (php,git,web,java,html)


----------


    <?php
    
    if (isset($_POST["submit"]))
    	{
    	echo $nume = $_POST["nume"] . "<br />";
    	echo $prenume = $_POST["prenume"] . "<br />";
    	echo $facultate = $_POST["facult"] . "<br />";
    	echo $specialitatea = $_POST["spec"] . "<br />";
    	echo $grupa = $_POST["grupa"] . "<br />";
    	echo $curs = $_POST["curs"] . "<br />";
    	}
    
    echo "===========" . "<br />";
    ?>
    <html>
    <head>
    <title>Page Title</title>
    </head>
    <body>
    
    <form method="post" action="">
      Nume: <input type="text" name="nume"/><br />
      Prenume: <input type="text" name="prenume"/><br />
      Facultatea: <input type="text" name="facult"/><br />
      Specialitatea: <input type="text" name="spec"/><br />
      Grupa: <input type="text" name="grupa"/><br />
      <select name="curs">
	    <option value="git" >Web</option>
    	<option value="web" >Web</option>
        <option value="java">Java</option>
        <option value="html">Html</option>
        <option value="php">Php</option>
      </select>
      <br />
      <input type="submit" name="submit">
    </form>
    
    </body>
    </html>




# Laboratorul Nr.4 

Verificam daca sunt numere pitagorice:

    <form method="POST" action="ex1.php">
       <H3> Introduceti 3 numere naturale nenule pentru a verifica daca sunt numere pitagorice: </H3>
       a = <input type="text" name="a" size="5" value=""> &nbsp;
       b = <input type="text" name="b" size="5" value=""> &nbsp;
       c = <input type="text" name="c" size="5" value=""> <br> <br>
       <input type="submit" name="submit" value="Verifica">
     </form>
     <br>
     <?php
       $n1 = @$_POST['a'];
       $n2 = @$_POST['b'];
       $n3 = @$_POST['c'];
       if(isset($_POST['submit'])){
         if(!empty($n1) && !empty($n2) && !empty($n3)){
    	   if(($n3 > $n1) && ($n3 > $n2))
    	     if($n1*$n1 + $n2*$n2 === $n3*$n3) {echo "Numerele ".$n1.", ".$n2." si ".$n3." sunt numere pitagorice.";}
    	    else echo "Numerele ".$n1.", ".$n2." si ".$n3." nu sunt numere pitagorice."; 
           if(($n2 > $n1) && ($n2 > $n3))
    		   if($n1*$n1 + $n3*$n3 === $n2*$n2) {echo "Numerele ".$n1.", ".$n2." si ".$n3." sunt numere pitagorice.";}
    	    else echo "Numerele ".$n1.", ".$n2." si ".$n3." nu sunt numere pitagorice."; 
           if(($n1 > $n2) && ($n1 > $n3))
    	       if($n2*$n2 + $n3*$n3 === $n1*$n1) {echo "Numerele ".$n1.", ".$n2." si ".$n3." sunt numere pitagorice.";}
    		else echo "Numerele ".$n1.", ".$n2." si ".$n3." nu sunt numere pitagorice.";      
       } else echo "Nu ai dat numere.";
       }
     ?>


----------
Aflam paritatea numarului.

    <form method="POST" action="">
       <H4>Aflati paritatea numarului: <H4>
       <input type="text" name="nr" size="5" value=""> <br> <br>
       <input type="submit" name="submit" value="Verifica">
     </form>
     <br> <br> 
     <?php
       $a = @$_POST['nr'];
       if(isset($_POST['submit'])){
         if($a != ""){
    	   if($a % 2 === 0)
    	     echo "Numarul ".$a." este numar par.";
    	   else echo "Numarul ".$a." este numar impar.";	         
       } else echo "Nu ai dat numar.";
       }
     ?>


----------
Generator 

    <form method="POST" action="">
       Introduceti 2 numere: <br> <br>
       x = <input type="text" name="x" size="5" value=""> &nbsp;
       y = <input type="text" name="y" size="5" value=""> <br> <br>
       <input type="submit" name="submit" value="Calculeaza">
     </form>
     <br> <br> 
     <?php
       $x = @$_POST['x'];
       $y = @$_POST['y'];
       if(isset($_POST['submit'])){
         if(($x != "") && ($y != "")){
    		    echo "Pentru $x si $y vom avea: <br>";
    			$a = 2 + $x - $y;
    			$b = $x*$a + $y;
    			$c = $a - 2*$b + $x;
    	        echo "A = 2 + x - y = ".$a."<br>";
    			echo "B = x*A + y = ".$b."<br>";
    			echo "C = A - 2*B + x = $c";
       } else echo "Nu ai dat numere.";
       }
     ?>


----------
Rezolvam sistemul de ecuatii.

    <form method="POST" action="ex4.php">
       <H4> Pentru a rezolva sistemul de ecuatii <br>
       a*x + b*y = 0 <br>
       &nbsp;&nbsp;&nbsp;&nbsp;x + c*y = 1 <br>
       introduceti coeficientii a, b si c </h4> 
       a = <input type="text" name="a" size="5" value=""> &nbsp;
       b = <input type="text" name="b" size="5" value=""> &nbsp;
       c = <input type="text" name="c" size="5" value=""> <br> <br>
       <input type="submit" name="submit" value="Afla x si y">
     </form>
     <br> <br> 
     <?php
       $a = @$_POST['a'];
       $b = @$_POST['b'];
       $c = @$_POST['c'];
       function solutia1($x1, $x2, $x3){
    	   $s = $x2/($x2 - $x1*$x3);
    	   return $s;
       }
       function solutia2($x1, $x2, $x3){
    	   $s = ((-1)*$x1)/($x2 - $x1*$x3);
    	   return $s;
       }
       if(isset($_POST['submit'])){
         if(($a != "") && ($b != "") && ($c != "")){
    	    echo $a."*x + ".$b."*y = 0<br>x + ".$c."*y = 1 <br>";
    		if(((-1)*$b + $a*$c) != "0"){
    			$x = solutia1($a, $b, $c);
    			$y = solutia2($a, $b, $c);
    			echo "Solutiile sisitemului sunt: <br>x = ".$x." &nbsp;&nbsp; si &nbsp;&nbsp; y = ".$y;
    		}else echo "Sistemul nu are solutii."	;	
       } else echo "Nu ai dat coeficientii.";
       }
     ?>


----------

Piramida de numere


    <?php
          function calc($a, $b){
    	    $d = $a.$b++;	  
    	    return ($d);
          }
          $z = NULL;
          for($i = 1; $i <= 9; $i++){
    	    $z = calc($z,$i);
    	    $j = $i + 1;
    	    $t = ($z*9) + $j;
    	    echo $z."*9 + ".$j." = ".$t."<br>";  
          }
        ?>


----------
Să se scrie un program care să afișeze următoarea “piramidă” de numere:

    n n-1 n-2 … 3 2 1
    n-1 n-2….…...2 1
    …………………..
    3 2 1
    2 1
    1 


----------


    <?php
    $i = 9;
    while($i > 0){
    echo $i." ";
    for($a = 1; $a < $i; $a++){
    echo $i - $a . " ";
    }
    echo "<br>";
    $i--;
    }
    ?>


----------


# Laboratorul Nr.5  -  *Lucrul cu fișierele*
Afisam datele dintr-un fisier oarecare .



     <?php
      $f = $_POST['file'];
      $numefile = "careva.txt";
      $f1 = fopen($numefile,"r");
      $info = fread($f1, filesize($numefile));
      print_r($info);
    ?>
    <html>
      <form action = "" method = "post">
        <label for="file"> Nume fisier: </label>
    	<input type="file" name="file" id="file"> <br>
    	<input type="submit" name="submit" value="Trimite">
      </form>
    </html>
    
    


----------

 # Laboratorul Nr.6  -  *Crearea bazelor de date*

Creăm baza de date cu un nume oarecare de exemplu **local_db**:

    <?php
      $server = "localhost";
      $user = "root";
      $pass = "";
    
      // ne conectam la bd
      $conn = new mysqli($server, $user, $pass);
      if ($conn->connect_error) {
          die("Conectare eronata: " . $conn->connect_error);
      } 
    
      // creem bd
      $sql = "CREATE DATABASE local_db";
      if ($conn->query($sql) === TRUE) {
          echo "Baza de date a fost creata cu succes! <br>";
      } else {
        echo "Erroare baza de date nu a fost creata: " . $conn->error . "<br>";
      }
      
      $conn->close();
    ?>

Creăm tabela **cursuri** in baza de date studenti:
**urmatorul cod demonstreaza asta**

    <?php
      $server = "localhost";
      $user = "root";
      $pass = "";
      $dbname = "local_db";
      
      // Create connection
      $conn = new mysqli($server, $user, $pass, $dbname);
      // Check connection
      if ($conn->connect_error) {
          die("Conectare eronata: " . $conn->connect_error);
      } 
    	  
      // sql to create table
      $sql = "CREATE TABLE cursuri (
      id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY, 
      nume VARCHAR(30) NOT NULL,
      prenume VARCHAR(30) NOT NULL,
      email VARCHAR(50)
      )";
    
      if ($conn->query($sql) === TRUE) {
          echo "Tabela Cursuri a fost creata cu succes!<br>";
      } else {
          echo "Eroare tabela nu a fost creata: " . $conn->error . "<br>";
      }
       
      $conn->close();
      
    ?>

Inserăm date în tabela **cursuri**:

    <?php
      $server = "localhost";
      $user = "root";
      $pass = "";
      $dbname = "local_db";
      
      // Create connection
      $conn = new mysqli($server, $user, $pass, $dbname);
      // Check connection
      if ($conn->connect_error) {
          die("Connectare eronata: " . $conn->connect_error);
      } 
    	  
      $sql = "INSERT INTO local_db (nume, lector, durata)
      VALUES ('php', 'Gasnas Ala', '4 saptamini');";
     $sql = "INSERT INTO local_db (nume, lector, durata)
      VALUES ('html', 'Braicov Andrei', '2 luni');";
     $sql = "INSERT INTO local_db (nume, lector, durata)
      VALUES ('c', 'Pavel Maria', '4 luni');";
     $sql = "INSERT INTO local_db (nume, lector, durata)
      VALUES ('java', 'Corlat Serghei', '6 luni');";

    
      if ($conn->multi_query($sql) === TRUE) {
          echo "Datele au fost introduse cu succes.";
      } else {
          echo "Eroare: " . $sql . "<br>" . $conn->error . "<br>";
      }  
      $conn->close();
    ?>

