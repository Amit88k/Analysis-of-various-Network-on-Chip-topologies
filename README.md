# Analysis-of-various-Network-on-Chip-topologies

Requirements:
1. Ubuntu or any unix based operating system with network simulator 2 (ns2), network
animator (nam) installed.
2. If not installed, run:
2.1. sudo apt-get install ns2
2.2. Now download and install nam 1.14 as default nam has development issues and
will give segmentation fault always. Download and install by:
(a) sudo apt-get purge nam
(b) wget --user-agent="Mozilla/5.0 (Windows NT 5.2; rv:2.0.1)
Gecko/20100101 Firefox/4.0.1"
"http://technobytz.com/wpcontent/uploads/2015/11/nam_1.14_amd64.zip"
(c) unzip nam_1.14_amd64.zip
(d) sudo dpkg -i nam_1.14_amd64.deb
(e) sudo apt-mark hold nam
3. This will install ns2 and nam on the system
4. Test nam by typing nam in terminal. Empty network animator must open up.
Procedure:
1. Extract project from major.tar.gz.
2. Open terminal.
3. Move into major and then into DropTail or DRR or RED or REM or FQ or SFQ folder
depending on the queue management technique required using cd command in terminal as
cd Major/DropTail for droptail, cd Major/DRR for drr and so on.
4. Now again using cd command in terminal move into the folder corresponding to the
required topology like FatTree16 for fat tree of 16 nodes, hybrid 4*4 for mesh of trees of
16 nodes and so on as cd FatTree16 or cd KingMesh.
5. Use shell script to run the program. Search in the required folder for corresponding shell
script file with source and destination considering 0 to be 1st node and 15 to be last in 16
node configuration and type the command:
a) For FatTree16, FatTree64, FatTree256: ./tree.sh
b) For Hybrid 4*4: ./grid_ls.sh 4 4 source destination
c) For Hybrid 8*8: ./grid_ls.sh 8 8 source destination
