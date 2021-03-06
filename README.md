# Ubuntu Install Software

<strong>Note: I just want to share somethings in Ubuntu 19.04 which are worked with me</strong>
<p>If you cannot install the latest version of Ubuntu, try to instsall the <strong>lower version</strong></p>

<h3>Fix: "Error Unable to 'apt update' my Ubuntu 19.04"  <a href="https://www.digitalocean.com/community/questions/unable-to-apt-update-my-ubuntu-19-04">Link </a> 
</h3>
<p> <strong>Note: </strong>If you install and get this problem, fix this error first before installing anything</p>
<pre>sudo sed -i -re 's/([a-z]{2}\.)?archive.ubuntu.com|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
sudo apt-get update && sudo apt-get dist-upgrade
</pre>

<h3>Install "Google Chrome"  <a href="https://linuxize.com/post/how-to-install-google-chrome-web-browser-on-ubuntu-18-04/">Link</a>
</h3>
<pre>wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
</pre>

<h3>Install "Git"</h3>
<p>Download Git</p>
<pre>sudo apt install git</pre>
<p>Check version</p>
<pre>git --version</pre>

<h3>Install "Jupyter Notebook"</h3>
<p>Download Git: <code>sudo apt-get install jupyter-notebook</code></p>
<p>Run: <code> jupyter notebook </code></p>


<h3>Install "Play On Linux" (applications: office, internet, educations, games,...</h3>
<p><code>sudo apt install winbind</code></p>
<p><code> sudo apt install playonlinux</code></p>
 
 
<h3>Update Python 3.8  <a href="https://www.itsupportwale.com/blog/how-to-upgrade-to-python-3-8-on-ubuntu-18-04-lts/">Link</a>
</h3>
<p>Follow all steps of the link above</p>
<p>While installing this command:</p>
<pre>sudo add-apt-repository ppa:deadsnakes/ppa</pre>
If there is error message:
<pre><i>Cannot add PPA: 'ppa:~deadsnakes/ubuntu/ppa'.
ERROR: '~deadsnakes' user or team does not exist.</i></pre>
Just fix it by adding '':
<pre>sudo add-apt-repository 'ppa:deadsnakes/ppa'</pre>   

<h3>Fix: Ubuntu 19.04 won't open terminal after Python 3.8.0 install</h3>
<ol>
 <li>Install <code>Xterm</code> from Ubuntu Software</li>
 <li>Type <code>sudo update-alternatives --config python3</code></li>
 <li>Choose "python3.7" as a default</li> 
</ol>

<h3>Fix: ModuleNotFoundError: No module named 'apt_pkg' <a href="https://stackoverflow.com/questions/13708180/python-dev-installation-error-importerror-no-module-named-apt-pkg">Link</a>
</h3>
<pre>cd /usr/lib/python3/dist-packages
ls (copy the right name of "apt_pkg")
sudo ln -s apt_pkg.cpython-36m-x86_64-linux-gnu.so apt_pkg.so</pre>

<h3>Install "Unikey" <a href="https://github.com/teni-ime/ibus-teni">Link</a>
</h3> 
<pre>sudo add-apt-repository ppa:teni-ime/ibus-teni
sudo apt-get update
sudo apt-get install ibus-teni
ibus restart
</pre>                                                                                                                               
While installing, if there is error message:
<pre><i>E: Could not get lock /var/lib/dpkg/lock-frontend - open (11: Resource temporarily unavailable)  
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend),   
 is another process using it?</i></pre>
<p>Then write command: </p>
<pre>sudo killall apt apt-get</pre>   
<p>Uninstall Software</p>
<pre>sudo apt remove ibus-teni
ibus restart
</pre>

<h3>Ip Address</h3>
<ol>
  <li>If you prefer to get minimal details, you can also use hostname:<code>hostname -I </code></li>
  <li>It will show you both IPv4 and IPv6 addresses: <code>ip a </code></li>
  <li>Same: <code>ip add</li>
</ol>
<img src="https://i1.wp.com/itsfoss.com/wp-content/uploads/2019/08/ip_addr_show.png?w=800&ssl=1">

<p> Beside that, I also installed some softwares which are already had in Software Ubuntu such as: 
 <i>Visual Studio, Sublime Text, Slack, ...</i>
</p>

<h3> </h3>
 <p>try <code>aptitude</code> instead of <code>apt-get</code><p>

  <code>sudo apt-get install aptitude</code>
  <code>sudo aptitude install <package-name> </code>

 
 <h3>Comment</h3>
 
 
 
 
