# SQL injection 

---

## PHP code vulnerable to SQL injection.

```php
<?php
    include "conect.php";

    $id = $_GET['input'];

    $qy = $con->prepare("SELECT username, email FROM users WHERE id=$id");

    $qy->execute();
    $users = $qy->fetch();
    $count = $qy->rowCount();
    
    echo "email is : " . $users['email'] . "<br>";
    echo "username is : " . $users['username'];

?>
```
