# Augmented Reality - HoloLens

MesoCraft supports streaming the scene content to HoloLens 2. The following steps need to be performed to make it run:

PREPARING HOLOLENS 2
- start HoloLens 2
- connect it to the same network as the computer from where MesoCraft is run
- start Holographic Remoting App on the HoloLens (can be found in Microsoft store)
- wait till an IP address is shown

RUNNING THE APP
- unzip MesoCraf.zip archive
- run MesoCraft.exe (if it does not run, respective additional Qt Release libraries might be required)
- input the IP address from Holographic Remoting App into the popup dialog
- press Space while the smaller of the two MesoCraft's window is focused (this will start the streaming)

?> Notice: if there is no popup dialog presented while MesoCraft starts, then MesoCraft was not built with HoloLens support. In that case, ask for a build.

