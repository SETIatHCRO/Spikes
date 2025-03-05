### Abstract

This guide walks through the necessary steps to access the lab computer running the SPIKES application via SSH. It allows the user to access the lab computer from within the local network of HCRO or from outside the network via VPN.

Note: This method is absolutely viable to perform measurements and browse the data, however, it is easier and an overall more enjoyable experience to use the SPIKES application on the local machine. 

### Running SPIKES

The first step is connecting to the computer, if you are on windows, activate WSL (Windows Subsystem for Linux) and use install a linux distribution of your choice via the microsoft store (you will have a command line interface ready after installing and creating a user). 

If you are on linux or mac open a terminal and type the following command:

```bash
ssh -Y sonata@10.1.23.153
# Be sure to use -Y for the GUI to work properly
```

After entering the password you will be connected to the computer. You can now run the application by typing the following command:

```bash
spikes
```

### Browsing the Measurements

In order to browse the measurements you will navigate to the Measurements directory thusly:

```bash
cd ~/SPIKES/Measurements
```

As described in the SPIKES README file, the folder structure is organized as follows:

```Folder Structure
Measurements
├── date[YYYY-MM-DD]
│   ├── time[HHhMM]-[config_name]
│   │   ├── data
│   │   │   ├── config file[config_name].yml
│   │   │   └── trace_n.csv
|   |   ├── imgs_legend
|   |   |   ├── combined_trace.png
|   |   |   └── trace_n.png
|   |   └── imgs_nolegend
|   |       ├── combined_trace.png
|   |       └── trace_n.png
```

To get measurement data from the lab computer to your local machine you can use the scp (Secure Copy) command:

```bash
scp -r user@address:/path/to/remote/directory /path/to/local/destination
# Using -r to copy directories, not necessary for single files
```

Example:

```bash
scp -r sonata@10.1.23.153: ~/SPIKES/Measurements /home/YourUserName/Somewhere
# This will copy the whole Measurements directory to Somewhere on your local machine
```

### Creating a new Configuration

To create a new configuration you will navigate to the Configuration directory:

```bash
cd ~/SPIKES/Configuration
```

Here you will find the configuration files for the SPIKES application. To create a new configuration you can copy an existing configuration file and modify it to your needs:

```bash
cp fast_template.yml my_splendid_config.yml
```

You can now edit the configuration file with your favorite text editor (for example nano):

```bash
nano my_splendid_config.yml
```

You will be rewarded with the following sight:

```yaml
### GNU nano x.x ############### my_splendid_config.yml ########
sweep_points:     1001      # number of points
start_freq:       300e6     # Hz
stop_freq:        10e9      # Hz
res_bw:           500e3     # Hz
vid_bw:           500e3     # Hz
attenuation:      10        # dB
mode:             FAST      # Mode of operation: HIGH-RES or FAST
# mode specific parameters
display_refresh:  1         # seconds (int or float)
integration_time: 5         # seconds (integer)
total_traces:     5         # integer or "cont" for continuous operation
```

After saving the edited file the configuration is ready to be used within the SPIKES application.

Please refer to the Git_Push_Guide for a reminder to always push your changes to the repository.
