# material-themes-v2
custom themes for mabinogi

If you make your own colour sets and wanna add it to the main project feel free to do a merge request!

if you use .it just drop the .it file into the package folder in mabi
if you use the data folder just drop that into the root folder in mabi (where client.exe is) and make sure to turn on "use data folder" in your patcher of choice


## examples

![gJKfWZKcUQ](https://user-images.githubusercontent.com/20039012/161009538-57bda99b-902c-413d-a6e5-165eb53312e7.png)
![wA0QjHCWh7](https://user-images.githubusercontent.com/20039012/161009547-e12e0803-a54a-465b-99c7-f4954eac09a4.png)
![HsnEB0hx1C](https://user-images.githubusercontent.com/20039012/161009560-e290389c-fafb-4671-a504-d2ee6532bce2.png)
![IESyRBRhad](https://user-images.githubusercontent.com/20039012/161009564-9f9014cf-d895-48b2-baba-d973a20693b4.png)
![4UhFGZPGSa](https://user-images.githubusercontent.com/20039012/161009568-d52bbf44-681d-4349-8c5f-78329a926323.png)
![uXL4gwUL96](https://user-images.githubusercontent.com/20039012/161009572-9af29850-5448-4b53-81e8-92b7d94f3189.png)
![PR2pid8Tm4](https://user-images.githubusercontent.com/20039012/161009578-b49e2d83-cdb0-4c2e-bb61-967165e5024c.png)
![DO2UCOLgla](https://user-images.githubusercontent.com/20039012/161009583-908147af-f919-49b8-8b22-1cdb28e6f43c.png)



If you ever want to make your own color edits for these themes, make a copy of "40_template.xml" inside /data/db/themepack

in this example edit i will be making a theme called "example"
first edit the name of your copy to be something like "41_example.xml"

edit these lines
```xml
	<Configuration Name="template" LocalName="template" Version="3" BaseTexturePath="data/themefiles/interface/template.dds" BaseRenderState="rs_image_alpha_mod_point"  Index="0" />
```
name and local name should be the name you want the theme
BaseTexturePath should be the path for you dds file that contains your colors or edit.
so if i wanted to make my theme i would edit it to be

```xml
	<Configuration Name="Example" LocalName="Example" Version="3" BaseTexturePath="data/themefiles/interface/example.dds" BaseRenderState="rs_image_alpha_mod_point"  Index="0" />
```
then starting on line 497 is this
```xml
		<!-- Soulstream's inventory -->
		<Image Type="imgSoulStream" x="198" y="0"  w="28" h="23" renderFunc="_FillIcon" path="data/themefiles/interface/LevelUpIncentive/template.dds" />
		<!-- Display current level of Level up Incentive -->
		<Image Type="imgCurrentLevelIncentive" x="281" y="1"  w="16" h="16" renderFunc="_FillIcon" path="data/themefiles/interface/LevelUpIncentive/template.dds" />
```
change "template.dss"
to the name of your dds
eg:
```xml
		<!-- Soulstream's inventory -->
		<Image Type="imgSoulStream" x="198" y="0"  w="28" h="23" renderFunc="_FillIcon" path="data/themefiles/interface/LevelUpIncentive/example.dds" />
		<!-- Display current level of Level up Incentive -->
		<Image Type="imgCurrentLevelIncentive" x="281" y="1"  w="16" h="16" renderFunc="_FillIcon" path="data/themefiles/interface/LevelUpIncentive/example.dds" />
```
after this go to the path /data/themefiles/interface
make a copy of template.dss
edit the copy to be how you want it
make sure to rename it to what you put above
do the same for template.dss inside /data/themefiles/interface/levelupincentive
