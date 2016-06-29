# h_ttp(http time test plus)
More convenient HTTP time measurement plugin for Munin

## Download
```
curl -O https://raw.githubusercontent.com/HimaJyun/Munin-h_ttp/master/h_ttp_
sudo mv h_ttp_ /usr/share/munin/plugins/
sudo chown root:root /usr/share/munin/plugins/h_ttp_
sudo chmod 755 /usr/share/munin/plugins/h_ttp_
```

## Settings
1. Use symbolic link.  
`sudo ln -s /usr/share/munin/plugins/h_ttp_ /etc/munin/plugins/h_ttp_(Unique name)`  
example:`sudo ln -s /usr/share/munin/plugins/h_ttp_ /etc/munin/plugins/h_ttp_homepage`
2. Open your munin-node setting.  
`sudo editor /etc/munin/plugin-conf.d/munin-node`
3. Please set.  
4. Restart your munin-node.  
`sudo service munin-node restart`
5. Make sure that it operates correctly.
6. Let's brag to girlfriend(s)!!
 
## Configuration
The following values are required.  
```
[h_ttp_(Unique name)]  
  env.url (URL)  
```
example:  
```
[h_ttp_homepage]  
  env.url http://localhost/  
```
You can disable compression if necessary.  
```
[h_ttp_(Unique name)]  
  env.compression off  
```
