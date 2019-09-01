Unraid is easy, and freaking rock solid.  Just takes a bit to learn your way around, and how to deploy the containers, but once you get it it's so simple.  Unraid itself couldnt be easier to set up.  
--Set up your flash drive using the instructions, https://wiki.unraid.net/USB_Flash_Drive_Preparation<br>
--Hook up all of your drives<br>
--Boot to flash drive.  <br>
--Give the server a static IP (I use a reservation in my router). <br> 
--Hit the web interface, add the drives to your array.  Ideally, you have an SSD you can set as the cache drive.  The rest are array devices. <br> 
--You will be prompted to format the drives, do it<br>
--Once your array is started and running<br>
--Enable docker - https://lime-technology.com/wp/docker-guide/ (you dont need to add the template repositories)<br>
--Add the community applications plugin https://lime-technology.com/forums/topic/38582-plug-in-community-applications/<br>
--Set up a few shares under the shares tab. <br> 
      --create a media share (image below of settings)<br>
      --create appdata share for containers persistent configs (image of settings attached)<br>
      --create subdirs for the media share (like tv, movies, etc...)<br> 
      (you can do this via ssh, or windows explorer if you enable SMB export in the <br>
      security settings under the media share, or some other way.<br>
      --create a share for downloads.  use cache set to only.<br>
      --create a share for tempdownloads.  use cache set to only.<br>
--use community applications to add your first container, use the containers by linuxserver whenever available.<br>  

****Container config****

This is pretty straightforward.  your appdata or config path will be /mnt/user/appdata, if you are setting up something like plex, your media directory will be /mnt/user/media, if you are setting up something like sab, your downloads path would be /mnt/cache/downloads and your incomplete downloads can be /mnt/cache/tempdownloads.  Typically the only other thing you need to set is the port.  The template will have a container port, usually already set (like 7878 for radarr).  It will ask you for a host port.  You can use anything you havent used before so start with like 10000 for the first container, 10001 for the second etc....  This is the port you will use to access the application interface.  so example: http://ipofunraidserver:10001

It really is that easy.  Add a UPS, set up a backup for your appdata folders and PROFIT.