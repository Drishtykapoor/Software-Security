# Software-Security
# CTFStalwarts

```
Our project is designed to help us identify and patch up possible vulnerabilities.
We have written 3 scripts to provide an aid in achieving this -

The first one is Escape Command Injection which is used to patch up command injection vulnerability. The second and third scripts are used to find possible exploits for SQL Injection and Path Traversal issues respectively.
```

## Prerequisites

```
Python 3.x.x
```

## Scripts

### EscapeCommandInjection

```
This script looks for system calls in the program which could be possible command injection vulnerabilities. It replaces these system calls with our own safe_system call functions which are not vulnerable to command injection attacks.
On running the script a new .c file is created which can be used instead of the previous vulnerable file.
```

### SQLInjectionExploit

```
This script was made in order to check for exploitation in Urls.
The script will parse each URL and try to generate an exploitable URL from them.
It will then check whether the param values contain an integer value or not.
If it finds any integer value then we add %27 after the number.
If it gets any error then we can assume it to be a weak URL and potential for SQL injection exploit.
The scripts additionally takes the start and end integers which signify the range of exploits to be done.
```

### PathTraversalExploit

```
This script was made in order to check for path traversal exploits in Urls.
The script will look for file as param value and replace the param values with /etc/passwords and /etc/hosts.
Request is made with updated URL to find path exploit.
```

## Running

### EscapeCommandInjection

```
python EscapeCommandInjection <filename>
```

### SQLInjectionExploit

```
python SQLInjectionExploit <url> <start> <end>
```

### PathTraversalExploit

```
python EscapeCommandInjection <url>
```

## Authors

* **AdhirajTikku@stalwarts**
* **ChenYang@stalwarts**
* **ChetanyaAhuja@stalwarts**
* **DrishtyKapoor@stalwarts**
* **SaurabhPrakash@stalwarts**
