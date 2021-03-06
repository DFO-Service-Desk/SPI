# SPI
## A) GPSC

1) First, log  : ssh -XC sdo000@gpsc-in
2) Secondly, log : ssh -XC sdo000@gpsc-vis6

3) To get access to the forecast read the link below:
http://www.gcpedia.gc.ca/wiki/DFO_GPSC#ECCC_Forecast_Products

**Actually, you only need to do these following lines because the .profile is already set:

export ORDENV_TRUEHOST=eccc-gpsc1
. ssmuse-sh -x eccc/cmo/cmoi/base/20180117

4) To load SPI follow the instructions:
http://www.gcpedia.gc.ca/wiki/DFO_GPSC#Viewer_and_software

5) The project is in the directory:
/fs/vnas_Hdfo/odis/sdfo000/sdfo000/ECCC_forecast/requests/CCG/Golf_of_Gothia/gulf_of_gothia_2.spi


## B) PPP
Log to group account : ssh -XC sdfo500@eccc-ppp2

The project is in the directory:
cd ~/SeDOO/requests/CCG/Gulf_of_Gothia/sample

## Generate forecast vidéo

1) Open SPI project:
- SPI
- Files/open_project : CCG_Gulf_of_Gothia.spi

4) Allez chercher les produits opérationnels (dans ce cas si - RIOPS pour Océan Artique) 
- cd $CMCGRIDF/prog/riops.native
- Files/open : select all the .std files of the last run of forecasts (ex. next 48 hours)
- Clic niveau/level 0.5 m, clic again niveau/level to sort
- Clic type P@, clic again type to sort
- Clic VAR select UUW and VVW, clic again VAR to sort
- Select the first UUW and VVW via [ctl] in VAR column
- Clic bottom left ''refresh diplay'' (blue arrow)

5) If there is a display problem:
- Open the console in the menu bar and write: fstdfield vector { UUW VVW }
- Clic on the wheel pictogram bar : Parameters
- Field /VAR  select the vectors display

6) Generate the figures for the video:
- Clic on animation in the menu bar
- run the animation with the save button (bottom rigth)
- After, in the linux command line run the following command where the files were produced to create the video:

convert -delay 500 title*.png name.gif

- to visualize the video :

gwenview name.gif

To bring back the video on local machine, see these examples :
  
scp sdfo500@eccc-ppp2:SeDOO/requests/CCG/Gulf_of_Gothia/test_version5_CCG_Gulf_of_Gothia_20180831.gif .

scp sdfo000@gpsc-in:/fs/vnas_Hdfo/odis/sdfo000/sdfo000/ECCC_forecast/requests/CCG/Golf_of_Gothia/test2_CCG_Gulf_of_Gothia_20180904UTC.gif .

***if you need to add your key .pub to the authorised keys please follow the procedure




