
**`nuget` Cheatsheet**
============

# To install

**Syntax:**
```
Install-Package <pkg name> -Version <version>
```

**Example:**
```cmd
Install-Package Spring.Data -Version 2.0.1
```
	

# To uninstall

**Synatx:**
```
Uninstall-Package <pkg name> -Version <version> –RemoveDependencies
```

**Example:**
```shell
Uninstall-Package Spring.Data -Version 2.0.1 –RemoveDependencies
```


# To Update
**Syntax:**
```shell
Update-Package <pkg name> -Version<version>
Update-Package <pkg name> -Version<version> -Reinstall
```
**Example:**
```shell
Update-Package Spring.Data -Version 2.0.1
Update-Package Spring.Data -Version 2.0.1 –reinstall
```

---
