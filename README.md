# Use pip install with python in user path to install external module (For HPC)

### Required command  ###
 
```
mkdir

wget

tar

make

make install

```

### Step 1: Create path & Download python  ###
 
```
mkdir ~/python3

cd ~/python3

wget https://www.python.org/ftp/python/3.6.0/Python-3.6.0.tgz

tar zxvf Python-3.6.0.tgz

cd Python-3.6.0

./configure --prefix='/work/username/python3' #username is the name of user account

make

make install

```


### Step 2: Set up python environment  ###

edit bashrc file

`vim /work/username/.bashrc`

append this line: `export PATH="/work/username/python3/bin:$PATH"`

`source .bashrc`

Then you can try `pip3 install numpy`
