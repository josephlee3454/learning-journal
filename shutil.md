# shutil 
* The shutil module includes high-level file operations such as copying and archiving.
## copying files 
* copyfile() copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.
### shutil_copyfile.py
### import glob
### import shutil

### print('BEFORE:', glob.glob('shutil_copyfile.*'))

### shutil.copyfile('shutil_copyfile.py', 'shutil_copyfile.py.copy')

### print('AFTER:', glob.glob('shutil_copyfile.*'))

## Because the function opens the input file for reading, regardless of its type, special files (such as Unix device nodes) cannot be copied as new special files with copyfile().
### $ python3 shutil_copyfile.py

### BEFORE: ['shutil_copyfile.py']
### AFTER: ['shutil_copyfile.py', 'shutil_copyfile.py.copy']