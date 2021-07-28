# PHP_APIExample
API Example ready to implement

## Setup

### Index file

#### Table on line 9

```
$table = "frameworks";

```

#### POST Method starting on line 25

Adaptar al tipo de objeto que se recibe. <br>
Adaptar la query.  <br>


```
if($_POST['METHOD']=='POST'){
    unset($_POST['METHOD']);
    $nombre=$_POST['nombre'];
    $lanzamiento=$_POST['lanzamiento'];
    $desarrollador=$_POST['desarrollador'];
    $query="insert into $table(nombre, lanzamiento, desarrollador) values ('$nombre', '$lanzamiento', '$desarrollador')";
    $queryAutoIncrement="select MAX(id) as id from $table";
    $result=putMethod($query, $queryAutoIncrement);
    echo json_encode($result);
    header($statusOk);
    exit();
}

```


#### PUT Method starting on line 38
