When you face problem like:
```
Checking for scripts.
Downloading scripts, this may take a little while
```
put the folder into `D:\miniconda\envs\<yourProject>\Lib\site-packages\visdom\static`
then change the `server\run_server.py`
in the end of the file:
```
def download_scripts_and_run():
### download_scripts()
    main()
```
