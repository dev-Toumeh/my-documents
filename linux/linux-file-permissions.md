# Understanding Linux File Permissions

## 1. Basics:
- **First character (`-` or `d`)**: `-` for a file, `d` for a directory.
- **Next three (`rwx`)**: Owner permissions (Read, Write, Execute).
- **Next three (`r-x`)**: Group permissions.
- **Last three (`r--`)**: Others (everyone else).

## 2. Changing File Permissions
- Examples:
  - `chmod 755 myfile.txt` → Owner: Read/Write/Execute, Group: Read/Execute, Others: Read/Execute.
  - `chmod 644 myfile.txt` → Owner: Read/Write, Group: Read, Others: Read.
  - `chmod +x script.sh` → Makes a file executable.

## 3. Changing File Ownership
- `chown user:group myfile.txt` → Changes owner and group.
- `chown -R user:group mydir/` → Recursively changes a directory.

## 4. Understanding Execute (`x`) Permission
### **For Files:**
- If a file is a script or program (`.sh`, `.py`, `.out`, etc.), the **execute permission allows you to run it**.
- Example:
  ```bash
  ./script.sh
  ```
### **For Directories:**
- **Execute permission on a directory** means you can **enter the directory (`cd directory/`) and access its contents**.
- Without `x`, you **cannot list or enter** the directory, even if you have read (`r`) permission.

## 5. What does numbers mean?:
- **(`6` → `rw-`)** → Read (`r`), Write (`w`), but **no execute (`-`)**.
- **(`5` → `r-x`)** → Read (`r`), Execute (`x`), but **no write (`-`)**.
