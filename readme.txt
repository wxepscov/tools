Version:
	Dump_AutoConfig 1.0
Relase Data:
	2019/12/10
Author:
	Bo Chen

Feature Enhancement:
	Develop dump auto config script
	Support below scenarios
	---BSOD issue dump config---
	1.check must use full dump or not , if yes, try to config full dump in avaliable disk
	2.check must use full dump or not , if no, config depend on the physical mememory
	a.If physical memory is above 32G, prefer to config kernel dump,pagefile use default value 20G,if has no enough disk free space to config 20G pagefile, try default value 6G
	b.If physical memory is below 32G, try to config full dump.If has no enough disk free space to config full dump, try to config kernel dump.If has no enough disk free space to config pagefile as physical memory size, try default value 6G
	---Hang issue dump config/Trigger dump requirement---
	1.check must use full dump or not , if yes, try to config full dump in avaliable disk
	2.check must use full dump or not , if no, config depend on the physical mememory
	a.If physical memory is above 32G, prefer to config kernel dump,pagefile use default value 20G,if has no enough disk free space to config 20G pagefile, try default value 6G
	b.If physical memory is below 32G, try to config full dump.If has no enough disk free space to config full dump, try to config kernel dump.If has no enough disk free space to config pagefile as physical memory size, try default value 6G
	---Restore Configuration which set by this script---
	Note:
	Add reserved_space option for disk usage protect,avoid performance risk
	Dumpflag: 0:nodump 1:fulldump 2:kernel dump
	Reportfile name: dumpconfig_##dateformat##.txt
	Orginal reg backup: orginalreg_backup.txt
Knownissue:
	N/A

Steps:
1.	Select the action to perform: 1.Dump Config  2.Restore Dump Config
2.	Select which scenario the dump used for: 1.BSOD  2.Hang
3.	Should we collect full dump file or not: 1.Yes 2.No
4.	Should we disable auto restart function: 1.Yes 2.No

Typical scenarios reference:
Scenario: BSOD + auto restart                                  Type: 1-1-2-2
Scenario: BSOD + disable auto restart                          Type: 1-1-2-1
Scenario: BSOD + full dump required+ auto restart              Type: 1-1-1-2
Scenario: BSOD + full dump required+ disable auto restart      Type: 1-1-1-1
Scenario: Hang + auto restart                                  Type: 1-2-2-2
Scenario: Hang + disable auto restart                          Type: 1-2-2-1
Scenario: Hang + full dump required+ auto restart              Type: 1-2-1-2
Scenario: Hang + full dump required+ disable auto restart      Type: 1-2-1-1
Scenario: Rollback dump auto configure                         Type: 2
