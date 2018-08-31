# SPI
Generate forecast vidéo 

1) use group account on ppp (so A & P have access):
ssh -XC sdfo500@eccc-ppp2

2) the project is in the directory
cd ~/SeDOO/requests/CCG/Gulf_of_Gothia/sample

3) Open SPI
- SPI
- Files/open_project : CCG_Gulf_of_Gothia.spi

4) Aller chercher les produits opérationnels (dans ce cas si - RIOPS pour Océan Artique) 
- cd $CMCGRIDF/prog/riops.native
- Files/open : select all the .fstd files of the last run of forecasts (ex. next 48 hours)
- Clic niveau/level 0.5 m, clic again niveau/level to sort
- Clic type P@, clic again type to sort
- Clic VAR select UUW and VVW, clic again VAR to sort
- Select the first UUW and VVW via [ctl] in VAR column
- Clic bottom left ''refresh diplay'' (blue arrow)

5) If problem in display
- Clic on the wheelin the pictogramm bar : Parameters
- Field /VAR  select the vectors display and the grid point
-





Ouvrir la console et inscrire : fstdfield vector { UUW VVW }




