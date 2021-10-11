# Git cmds

# Init
Ein leeres Git-Repository erstellen oder ein bestehendes neuinitialisieren

```bash
git init 
```

# Clone 
Ein Repository in einem neuen Verzeichnis klonen.

```bash
git clone 
```

## Wichtige Flags
```bash
-b <name>, --branch <name>
           Instead of pointing the newly created HEAD to the branch pointed to by the cloned repository's HEAD, point to <name> branch instead. In a
           non-bare repository, this is the branch that will be checked out.  --branch can also take tags and detaches the HEAD at that commit in the
           resulting repository.

<directory>
            The name of a new directory to clone into.         
```

## Beispiel 
```bash
git clone git://git.kernel.org/pub/scm/.../linux.git my-linux
cd my-linux
```
Kopiert von der Quelle "git://git.kernel.org/pub/scm/.../linux.git" das Repository und legt es im neuen Ordner "my-linux" ab.

# Branch
Branches anzeigen, erstellen oder entfernen.

```bash
git branch 
```

## Wichtige Flags
```bash
-d, --delete
           Delete a branch. The branch must be fully merged in its upstream branch, or in HEAD if no upstream was set with --track or --set-upstream-to.

-D
           Shortcut for --delete --force.

-a, --all
           List both remote-tracking branches and local branches. Combine with --list to match optional pattern(s).

-l, --list
           List branches. With optional <pattern>..., e.g.  git branch --list 'maint-*', list only the branches that match the pattern(s).

--show-current
           Print the name of the current branch. In detached HEAD state, nothing is printed.

<branchname>
           The name of the branch to create or delete. The new branch name must pass all checks defined by git-check-ref-format(1). Some of these checks may
           restrict the characters allowed in a branch name.
```

## Beispiel 
```bash
git branch my2.6.14 (1)
git branch -d my2.6.13 (2)
```
(1) Erstellt ein neuen Branch mit dem Namen "my2.6.14".
(2) Löscht den Branch mit dem Namen "my2.6.13"

# Switch
Branches wechseln.

```bash
git switch 
```

## Wichtige Flags
```bash
-c <new-branch>, --create <new-branch>
           Create a new branch named <new-branch> starting at <start-point> before switching to the branch. This is a convenient shortcut for:

               $ git branch <new-branch>
               $ git switch <new-branch>
<branch>
           Branch to switch to.              
```

# Beispiel 
```bash
git switch my2.6.14
```
Wechselt das aktuelle lokale Verzeichnis zu dem Branch "my2.6.14"  

# Status
Den Zustand des Arbeitsverzeichnisses anzeigen.

```bash
git status 
```

# Fetch
Objekte und Referenzen von einem anderen Repository herunterladen.

```bash
git fetch 
```

# Pull
Objekte von einem externen Repository anfordern und sie mit einem anderen Repository oder einem lokalen Branch zusammenführen.

```bash
git pull 
```

## Wichtige Flags
```bash

```

# Add 
Dateiinhalte zum Commit vormerken.

```bash
git add 
```

## Wichtige Flags
```bash
-A
```

# Commit
Änderungen in das Repository eintragen.

```basch 
git commit
```
## Flags
```bash
-A
```

## Wichtige Flags

# Push
Remote-Referenzen mitsamt den verbundenen Objekten aktualisieren.

```bach
git push
```

## Wichtige Flags
```bash
-A
```


# .gitignore
Dies ist ein File, welcher festlegt welche dateien nicht syncronisirt werden.

```bash
# Build Ordner 
build/**

## Beispiel für C/C++
# Object files
*.o
*.ko
*.obj
*.elf

# Libraries
*.lib
*.a
*.la
*.lo

# CMake
CMakeLists.txt.user
CMakeCache.txt
CMakeFiles
CMakeScripts
Testing
Makefile
cmake_install.cmake
install_manifest.txt
compile_commands.json
CTestTestfile.cmake
_deps

# VisualStudioCode
.vscode/*
!.vscode/settings.json
!.vscode/tasks.json
!.vscode/launch.json
!.vscode/extensions.json
*.code-workspace

##### MacOS
# General
.DS_Store
.AppleDouble
.LSOverride

##### Windows
# Windows thumbnail cache files
Thumbs.db
Thumbs.db:encryptable
ehthumbs.db
ehthumbs_vista.db

# Dump file
*.stackdump

# Folder config file
[Dd]esktop.ini

# Recycle Bin used on file shares
$RECYCLE.BIN/

# Windows Installer files
*.cab
*.msi
*.msix
*.msm
*.msp

# Windows shortcuts
*.lnk

```

