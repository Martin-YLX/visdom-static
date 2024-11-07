# Troubleshooting: Visdom Script Download Issue

If you encounter the following message when running Visdom:

```
Checking for scripts.
Downloading scripts, this may take a little while
```

Follow these steps to resolve the issue:

1. **Move the Folder**
   
   Place the folder into the following directory:
   
   ```
   D:\miniconda\envs\<yourProject>\Lib\site-packages\visdom\static
   ```

   Replace `<yourProject>` with the name of your specific project environment.

2. **Modify the Server Script**

   Locate the file `run_server.py` in the `server` directory and make the following change at the end of the file:

   ```python
   def download_scripts_and_run():
       # Comment out the download_scripts() line
       # download_scripts()
       main()
   ```

   By commenting out the `download_scripts()` line and directly calling `main()`, you can skip the script download step.

