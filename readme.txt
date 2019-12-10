Author:
Bo Chen

Steps:
1.	select the action to perform: 1.Dump Config  2.Restore Dump Config
2.	select which scenario the dump used for: 1.BSOD  2.Hang
3.	Should we collect full dump file or not: 1.Yes 2.No
4.	Should we disable auto restart function: 1.Yes 2.No

Typical scenarios:
Scenario: BSOD + auto restart                                  Type: 1-1-2-2
Scenario: BSOD + disable auto restart                          Type: 1-1-2-1
Scenario: BSOD + full dump required+ auto restart              Type: 1-1-1-2
Scenario: BSOD + full dump required+ disable auto restart      Type: 1-1-1-1
Scenario: Hang + auto restart                                  Type: 1-2-2-2
Scenario: Hang + disable auto restart                          Type: 1-2-2-1
Scenario: Hang + full dump required+ auto restart              Type: 1-2-1-2
Scenario: Hang + full dump required+ disable auto restart      Type: 1-2-1-1
Scenario: Rollback dump auto configure                         Type: 2
