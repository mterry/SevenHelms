# MUD2.BAS - Complete State Diagram

This is a complete state diagram showing all line labels as states and GOTO statements as transitions.

```mermaid
stateDiagram-v2
    [*] --> S0

    %% States by Category
    %% BattleAdv
    S1000 : 1000: What would you like to do?
    S1007 : 1007: Do you want to save? <Y/N>
    S1011 : 1011: What do you want to do?
    S1012 : 1012: Input
    S1013 : 1013: End
    S1020 : 1020: What would you like to do?
    S1070 : 1070: You attempt to parry the 
    S1080 : 1080
    S1090 : 1090
    S1510 : 1510: End

    %% BattleBasic
    S2000 : 2000: RANDOMIZE TIMER
    S2001 : 2001: PlayerReflect% = 0
    S2500 : 2500: End
    S2999 : 2999: COLOR 15

    %% CharCreation
    S0 : 0: Clear Screen
    S1 : 1: What would you like to do?
    S1_05 : 1.05: Clear Screen
    S1_1 : 1.1: What is your choice? <1-3>
    S1_2 : 1.2: Clear Screen
    S1_25 : 1.25: What is your choice?
    S1_3 : 1.3: Clear Screen
    S1_35 : 1.35: What is your choice?
    S1_7 : 1.7: End
    S10 : 10: Input
    S11 : 11: The 
    S12 : 12: The 
    S13 : 13: The 
    S14 : 14: The 
    S15 : 15: Input
    S16 : 16: The 
    S20 : 20: What would you like to do?
    S21 : 21: Please select 
    S21_5 : 21.5: Choose your familiar:
    S22 : 22: RANDOMIZE TIMER
    S24 : 24: Do you wish to redo the charac
    S25 : 25: End
    S27 : 27: End

    %% Encampment
    S700 : 700: Clear Screen
    S705 : 705: Input
    S710 : 710: Clear Screen
    S715 : 715: Input
    S720 : 720: Clear Screen
    S725 : 725: Input
    S730 : 730: Clear Screen
    S735 : 735: Input
    S740 : 740: Clear Screen
    S745 : 745: Input
    S750 : 750: Clear Screen
    S755 : 755: Input
    S760 : 760: Clear Screen
    S765 : 765: Input
    S770 : 770: Clear Screen
    S775 : 775: Input
    S780 : 780: Clear Screen
    S785 : 785: Input
    S790 : 790: Clear Screen
    S795 : 795: Input
    S800 : 800: Clear Screen
    S805 : 805: Input
    S810 : 810: Clear Screen
    S813 : 813: Input
    S815 : 815: Clear Screen
    S817 : 817: Input
    S818 : 818: Input
    S820 : 820: Clear Screen
    S825 : 825: Input
    S830 : 830: Clear Screen
    S835 : 835: Input
    S840 : 840: Clear Screen
    S845 : 845: Input
    S850 : 850: Clear Screen
    S855 : 855: Input
    S860 : 860: Clear Screen
    S865 : 865: Input
    S870 : 870: Clear Screen
    S875 : 875: Input
    S880 : 880: Clear Screen
    S885 : 885: Input
    S890 : 890: Clear Screen
    S895 : 895: Input
    S900 : 900: Clear Screen
    S905 : 905: Input
    S907 : 907: Input
    S910 : 910: Clear Screen
    S915 : 915: Input
    S917 : 917: Input
    S920 : 920: Clear Screen
    S925 : 925: Input
    S930 : 930: Clear Screen
    S935 : 935: Input
    S937 : 937: Input
    S940 : 940: Clear Screen
    S945 : 945: Input
    S947 : 947: Input
    S950 : 950: Clear Screen
    S955 : 955: Input
    S960 : 960: Clear Screen
    S965 : 965: Input
    S967 : 967: Input
    S970 : 970: Clear Screen
    S975 : 975: Input
    S977 : 977: Input
    S980 : 980: Clear Screen
    S985 : 985: Input
    S987 : 987: Input
    S990 : 990: Clear Screen
    S995 : 995: Input
    S996 : 996: COLOR 5
    S997 : 997: Input
    S998 : 998: Vampire> So do you wan't anoth
    S999 : 999: End

    %% Level1
    S209 : 209: Clear Screen
    S210 : 210: Input
    S215 : 215: Do you wish to save <Y/N>?
    S220 : 220: Clear Screen
    S225 : 225: Input
    S230 : 230: Clear Screen
    S235 : 235: COLOR 15
    S236 : 236: Input
    S240 : 240: Clear Screen
    S241 : 241: Clear Screen
    S245 : 245: Input
    S250 : 250: Clear Screen
    S255 : 255: Input
    S260 : 260: Clear Screen
    S265 : 265: Input
    S270 : 270: Clear Screen
    S275 : 275: Input
    S280 : 280: Clear Screen
    S285 : 285: Input
    S290 : 290: Clear Screen
    S295 : 295: Input
    S300 : 300: Clear Screen
    S305 : 305: Input
    S310 : 310: Clear Screen
    S315 : 315: Input
    S320 : 320: Clear Screen
    S325 : 325: Input
    S330 : 330: Clear Screen
    S335 : 335: Input
    S340 : 340: Clear Screen
    S345 : 345: Input
    S350 : 350: Clear Screen
    S355 : 355: Input
    S360 : 360: Clear Screen
    S365 : 365: Input
    S370 : 370: Clear Screen
    S375 : 375: Input
    S380 : 380: Clear Screen
    S385 : 385: Input
    S390 : 390: Clear Screen
    S395 : 395: Input

    %% Level2_3
    S500 : 500: Clear Screen
    S505 : 505: Input
    S510 : 510: Clear Screen
    S515 : 515: Input
    S520 : 520: Clear Screen
    S525 : 525: Input
    S530 : 530: Clear Screen
    S535 : 535: Input
    S540 : 540: Clear Screen
    S545 : 545: Input
    S550 : 550: Clear Screen
    S555 : 555: Input
    S560 : 560: Clear Screen
    S565 : 565: Input
    S570 : 570: Clear Screen
    S575 : 575: Input
    S580 : 580: Clear Screen
    S585 : 585: Input
    S590 : 590: Clear Screen
    S595 : 595: Input
    S600 : 600: Clear Screen
    S605 : 605: Input
    S610 : 610: Clear Screen
    S615 : 615: Input
    S620 : 620: Clear Screen
    S625 : 625: Input
    S630 : 630: Clear Screen
    S635 : 635: Input
    S640 : 640: Clear Screen
    S645 : 645: Input
    S650 : 650: Clear Screen
    S655 : 655: Input
    S660 : 660: Clear Screen
    S665 : 665: Input
    S670 : 670: Clear Screen
    S675 : 675: Input
    S677 : 677: Do you wish to save <Y/N>?
    S680 : 680: Clear Screen
    S685 : 685: Input
    S690 : 690: Clear Screen
    S695 : 695: Input

    %% MagicBoss
    S3000 : 3000: End
    S3001 : 3001
    S3002 : 3002
    S3003 : 3003
    S3004 : 3004
    S3005 : 3005
    S3006 : 3006
    S3007 : 3007
    S3008 : 3008
    S3009 : 3009
    S3010 : 3010
    S3011 : 3011
    S3012 : 3012
    S3013 : 3013
    S3014 : 3014
    S3015 : 3015
    S3016 : 3016
    S3017 : 3017
    S3018 : 3018
    S3019 : 3019
    S3020 : 3020
    S3021 : 3021
    S3022 : 3022
    S3023 : 3023
    S3024 : 3024
    S3025 : 3025
    S3026 : 3026
    S3027 : 3027
    S3028 : 3028
    S3029 : 3029
    S3030 : 3030
    S3031 : 3031
    S3032 : 3032
    S3033 : 3033
    S3034 : 3034
    S3035 : 3035
    S3036 : 3036
    S3037 : 3037
    S3038 : 3038
    S3039 : 3039
    S3040 : 3040
    S3041 : 3041
    S3042 : 3042
    S3043 : 3043
    S3044 : 3044
    S3045 : 3045
    S3046 : 3046
    S3047 : 3047
    S3048 : 3048
    S3049 : 3049
    S3050 : 3050
    S3051 : 3051
    S3052 : 3052
    S3053 : 3053
    S3054 : 3054
    S3055 : 3055
    S3056 : 3056
    S3057 : 3057
    S3058 : 3058
    S3059 : 3059
    S3060 : 3060
    S3061 : 3061
    S3062 : 3062: You freeze your opponent!
    S3063 : 3063
    S3064 : 3064
    S3065 : 3065
    S3066 : 3066
    S3067 : 3067
    S3068 : 3068
    S3069 : 3069
    S3070 : 3070
    S3071 : 3071
    S3072 : 3072
    S3073 : 3073
    S3074 : 3074
    S3075 : 3075
    S3076 : 3076
    S3077 : 3077
    S3078 : 3078
    S3079 : 3079
    S3080 : 3080
    S3081 : 3081
    S3082 : 3082
    S3083 : 3083
    S3084 : 3084
    S3085 : 3085
    S3086 : 3086
    S3087 : 3087
    S3088 : 3088
    S3089 : 3089
    S3090 : 3090: Lightning never strikes twice!
    S3091 : 3091
    S3092 : 3092
    S3093 : 3093
    S3094 : 3094
    S3095 : 3095
    S3096 : 3096
    S3097 : 3097
    S3098 : 3098
    S3099 : 3099
    S3100 : 3100
    S3500 : 3500: IF StunTime% = 0 THEN Xanathus
    S3600 : 3600
    S3700 : 3700: You attempt to parry Xanathus'
    S3800 : 3800
    S3900 : 3900
    S3950 : 3950: As Xanathus attacks, you attem
    S3975 : 3975: IF XanathusHP% <= 3 THEN
    S3976 : 3976: Xanathus casts a spell of curi
    S3977 : 3977: Xanathus casts magic arrow!
    S3978 : 3978: Xanathus casts Hand of Dust!
    S3979 : 3979: Xanathus prepares to flee!
    S3980 : 3980: RANDOMIZE TIMER
    S3989 : 3989: 'Miscasts
    S3990 : 3990: End

    %% Menu
    S9900 : 9900: End
    S9998 : 9998: Clear Screen
    S9999 : 9999: Input
    S10000 : 10000: End
    S10000_1 : 10000.1: End
    S10000_15 : 10000.15: Your owl spell list:
    S10100 : 10100: As the 
    S10110 : 10110: IF ENEMYPTS% <= 3 THEN

    %% NecroBattle
    S35000 : 35000: What would you like to do?
    S36000 : 36000: What would you like to do?
    S37000 : 37000: You attempt to parry Necrotali
    S38000 : 38000
    S39000 : 39000
    S39500 : 39500: As Necrotalia attacks, you att
    S39750 : 39750: IF NecrotaliaHP% <= 30 THEN
    S39760 : 39760: Necrotalia stands there and la
    S39770 : 39770: Necrotalia casts fire
    S39780 : 39780: Necrotalia casts Gaze of Death
    S39790 : 39790: Necrotalia jumps forward and s
    S39800 : 39800: Necrotalia casts hand of dust!
    S39890 : 39890
    S39900 : 39900: End

    %% NecroFight
    S1000000 : 1000000: Clear Screen
    S1000005 : 1000005: Input

    %% Other
    S0_1 : 0.1: RANDOMIZE TIMER               
    S0_2 : 0.2: RANDOMIZE TIMER               
    S0_9 : 0.9: Equip what in the Right Hand?
    S70 : 70: You attempt to parry the 
    S80 : 80
    S90 : 90
    S100 : 100: As the 
    S110 : 110: IF ENEMYPTS% <= 3 THEN
    S4000 : 4000: RANDOMIZE TIMER
    S4001 : 4001: StunTime% = 0
    S5000 : 5000: COLOR 15
    S19999_9 : 19999.9: RANDOMIZE TIMER
    S40000 : 40000
    S40010 : 40010

    %% SaveLoad
    S99998 : 99998: Which save posistion do you wa
    S99999 : 99999: Which save game do you wish to
    S100000 : 100000: End
    S100001 : 100001: End
    S100002 : 100002: End
    S101010 : 101010: End
    S102000 : 102000: RANDOMIZE TIMER
    S102001 : 102001: PlayerReflect% = 0

    %% Shop
    S400 : 400: End
    S410 : 410: End
    S430 : 430: COLOR 2
    S431 : 431: Input
    S445 : 445: IF Quest% = 1 THEN
    S450 : 450: COLOR 5
    S460 : 460: displayinventory
    S470 : 470: End

    %% Transitions (GOTO statements)
    S0 --> S0
    S0_9 --> S410
    S1 --> S1
    S1 --> S20
    S1 --> S2000
    S1_1 --> S1_1
    S1_1 --> S1_2
    S1_1 --> S1_3
    S1_1 --> S1_7
    S1_25 --> S1_05
    S1_25 --> S1_25
    S1_35 --> S1_05
    S1_35 --> S1_3
    S1_35 --> S1_35
    S1_7 --> S9900
    S10 --> S10
    S10 --> S21
    S11 --> S2500
    S12 --> S2500
    S13 --> S2500
    S15 --> S15
    S15 --> S2500
    S16 --> S2500
    S20 --> S20
    S20 --> S70
    S20 --> S80
    S20 --> S90
    S20 --> S100
    S20 --> S110
    S20 --> S2000
    S20 --> S2001
    S21 --> S21
    S21 --> S21_5
    S21_5 --> S21_5
    S21_5 --> S22
    S22 --> S22
    S22 --> S24
    S24 --> S0
    S24 --> S24
    S24 --> S25
    S25 --> S101010
    S27 --> S1510
    S70 --> S20
    S80 --> S20
    S80 --> S2000
    S90 --> S20
    S90 --> S2000
    S100 --> S20
    S110 --> S2000
    S210 --> S209
    S210 --> S210
    S210 --> S220
    S210 --> S240
    S215 --> S210
    S215 --> S215
    S225 --> S220
    S225 --> S225
    S225 --> S230
    S235 --> S220
    S235 --> S240
    S236 --> S210
    S236 --> S230
    S236 --> S235
    S236 --> S236
    S240 --> S241
    S241 --> S241
    S245 --> S230
    S245 --> S241
    S245 --> S245
    S245 --> S250
    S250 --> S250
    S255 --> S225
    S255 --> S240
    S255 --> S250
    S255 --> S255
    S255 --> S260
    S255 --> S270
    S260 --> S260
    S265 --> S250
    S265 --> S260
    S265 --> S265
    S265 --> S270
    S265 --> S290
    S265 --> S300
    S270 --> S270
    S275 --> S225
    S275 --> S250
    S275 --> S260
    S275 --> S270
    S275 --> S275
    S275 --> S280
    S275 --> S310
    S280 --> S270
    S285 --> S270
    S285 --> S280
    S285 --> S285
    S285 --> S320
    S290 --> S290
    S295 --> S260
    S295 --> S290
    S295 --> S295
    S300 --> S300
    S305 --> S260
    S305 --> S300
    S305 --> S305
    S305 --> S310
    S305 --> S330
    S310 --> S310
    S315 --> S225
    S315 --> S270
    S315 --> S300
    S315 --> S310
    S315 --> S315
    S315 --> S320
    S315 --> S360
    S320 --> S320
    S325 --> S280
    S325 --> S310
    S325 --> S320
    S325 --> S325
    S325 --> S340
    S330 --> S330
    S335 --> S300
    S335 --> S330
    S335 --> S335
    S335 --> S500
    S340 --> S340
    S345 --> S320
    S345 --> S340
    S345 --> S345
    S345 --> S350
    S355 --> S340
    S355 --> S350
    S355 --> S355
    S360 --> S360
    S365 --> S300
    S365 --> S310
    S365 --> S365
    S365 --> S370
    S365 --> S380
    S365 --> S390
    S370 --> S370
    S375 --> S360
    S375 --> S370
    S375 --> S375
    S380 --> S380
    S385 --> S360
    S385 --> S380
    S385 --> S385
    S390 --> S390
    S395 --> S360
    S395 --> S390
    S395 --> S395
    S400 --> S0_9
    S431 --> S431
    S431 --> S445
    S431 --> S450
    S431 --> S460
    S431 --> S470
    S445 --> S431
    S450 --> S430
    S460 --> S430
    S470 --> S100001
    S500 --> S500
    S505 --> S330
    S505 --> S500
    S505 --> S505
    S505 --> S510
    S510 --> S510
    S515 --> S500
    S515 --> S510
    S515 --> S515
    S515 --> S520
    S515 --> S530
    S515 --> S540
    S520 --> S520
    S525 --> S510
    S525 --> S520
    S525 --> S525
    S525 --> S530
    S525 --> S570
    S525 --> S620
    S530 --> S530
    S535 --> S510
    S535 --> S520
    S535 --> S530
    S535 --> S535
    S535 --> S550
    S535 --> S570
    S540 --> S540
    S545 --> S510
    S545 --> S540
    S545 --> S545
    S545 --> S550
    S545 --> S630
    S550 --> S550
    S555 --> S530
    S555 --> S540
    S555 --> S550
    S555 --> S555
    S555 --> S560
    S555 --> S640
    S560 --> S560
    S565 --> S550
    S565 --> S560
    S565 --> S565
    S570 --> S570
    S575 --> S520
    S575 --> S530
    S575 --> S570
    S575 --> S575
    S575 --> S580
    S585 --> S570
    S585 --> S580
    S585 --> S585
    S585 --> S590
    S595 --> S580
    S595 --> S590
    S595 --> S595
    S595 --> S600
    S595 --> S610
    S605 --> S590
    S605 --> S600
    S605 --> S605
    S615 --> S590
    S615 --> S610
    S615 --> S615
    S625 --> S520
    S625 --> S620
    S625 --> S625
    S625 --> S650
    S635 --> S540
    S635 --> S630
    S635 --> S635
    S635 --> S640
    S645 --> S550
    S645 --> S630
    S645 --> S640
    S645 --> S645
    S655 --> S620
    S655 --> S650
    S655 --> S655
    S655 --> S660
    S655 --> S670
    S655 --> S990
    S665 --> S660
    S665 --> S665
    S665 --> S670
    S675 --> S660
    S675 --> S670
    S675 --> S675
    S675 --> S750
    S677 --> S675
    S677 --> S677
    S685 --> S680
    S685 --> S685
    S685 --> S690
    S685 --> S750
    S685 --> S760
    S695 --> S680
    S695 --> S690
    S695 --> S695
    S695 --> S700
    S705 --> S690
    S705 --> S700
    S705 --> S705
    S705 --> S710
    S705 --> S770
    S715 --> S700
    S715 --> S710
    S715 --> S715
    S715 --> S720
    S725 --> S710
    S725 --> S720
    S725 --> S725
    S725 --> S730
    S725 --> S780
    S735 --> S720
    S735 --> S730
    S735 --> S735
    S735 --> S740
    S745 --> S730
    S745 --> S740
    S745 --> S745
    S745 --> S750
    S745 --> S790
    S755 --> S670
    S755 --> S680
    S755 --> S740
    S755 --> S750
    S755 --> S755
    S755 --> S800
    S765 --> S680
    S765 --> S760
    S765 --> S765
    S775 --> S700
    S775 --> S770
    S775 --> S775
    S785 --> S720
    S785 --> S780
    S785 --> S785
    S795 --> S740
    S795 --> S790
    S795 --> S795
    S805 --> S750
    S805 --> S800
    S805 --> S805
    S805 --> S810
    S813 --> S800
    S813 --> S810
    S813 --> S813
    S813 --> S815
    S815 --> S815
    S817 --> S810
    S817 --> S820
    S818 --> S815
    S818 --> S817
    S818 --> S818
    S820 --> S820
    S825 --> S815
    S825 --> S820
    S825 --> S825
    S825 --> S830
    S830 --> S830
    S835 --> S820
    S835 --> S830
    S835 --> S835
    S835 --> S840
    S835 --> S850
    S840 --> S840
    S845 --> S830
    S845 --> S840
    S845 --> S845
    S845 --> S850
    S845 --> S870
    S845 --> S880
    S845 --> S950
    S845 --> S970
    S850 --> S850
    S855 --> S830
    S855 --> S840
    S855 --> S850
    S855 --> S855
    S855 --> S860
    S855 --> S880
    S855 --> S890
    S855 --> S980
    S860 --> S860
    S865 --> S850
    S865 --> S860
    S865 --> S865
    S865 --> S870
    S865 --> S880
    S865 --> S890
    S865 --> S910
    S865 --> S920
    S870 --> S870
    S875 --> S840
    S875 --> S860
    S875 --> S870
    S875 --> S875
    S875 --> S880
    S875 --> S920
    S875 --> S940
    S875 --> S950
    S880 --> S880
    S880 --> S990
    S885 --> S840
    S885 --> S850
    S885 --> S860
    S885 --> S870
    S885 --> S880
    S885 --> S885
    S890 --> S890
    S895 --> S850
    S895 --> S860
    S895 --> S890
    S895 --> S895
    S895 --> S900
    S900 --> S900
    S905 --> S890
    S907 --> S900
    S907 --> S905
    S907 --> S907
    S910 --> S910
    S915 --> S860
    S917 --> S910
    S917 --> S915
    S917 --> S917
    S920 --> S920
    S925 --> S860
    S925 --> S870
    S925 --> S920
    S925 --> S925
    S925 --> S930
    S930 --> S930
    S935 --> S920
    S937 --> S930
    S937 --> S935
    S937 --> S937
    S940 --> S940
    S945 --> S870
    S947 --> S940
    S947 --> S945
    S947 --> S947
    S950 --> S950
    S955 --> S840
    S955 --> S870
    S955 --> S950
    S955 --> S955
    S955 --> S960
    S960 --> S960
    S965 --> S950
    S967 --> S960
    S967 --> S965
    S967 --> S967
    S970 --> S970
    S975 --> S840
    S977 --> S970
    S977 --> S975
    S977 --> S977
    S980 --> S980
    S985 --> S850
    S987 --> S980
    S987 --> S985
    S987 --> S987
    S995 --> S995
    S997 --> S11
    S997 --> S12
    S997 --> S13
    S997 --> S14
    S997 --> S16
    S997 --> S935
    S997 --> S990
    S997 --> S995
    S997 --> S996
    S998 --> S998
    S998 --> S999
    S999 --> S230
    S999 --> S350
    S999 --> S650
    S1000 --> S1000
    S1000 --> S1020
    S1000 --> S102000
    S1007 --> S27
    S1007 --> S1007
    S1012 --> S1011
    S1012 --> S1012
    S1012 --> S1013
    S1013 --> S5000
    S1020 --> S1020
    S1020 --> S1070
    S1020 --> S1080
    S1020 --> S1090
    S1020 --> S10100
    S1020 --> S10110
    S1020 --> S102000
    S1020 --> S102001
    S1070 --> S1020
    S1080 --> S1020
    S1080 --> S102000
    S1090 --> S1020
    S1090 --> S102000
    S1510 --> S400
    S2000 --> S2001
    S2999 --> S3000
    S2999 --> S3001
    S2999 --> S3002
    S2999 --> S3003
    S2999 --> S3004
    S2999 --> S3005
    S2999 --> S3006
    S2999 --> S3007
    S2999 --> S3008
    S2999 --> S3009
    S2999 --> S3010
    S2999 --> S3011
    S2999 --> S3012
    S2999 --> S3013
    S2999 --> S3014
    S2999 --> S3015
    S2999 --> S3016
    S2999 --> S3017
    S2999 --> S3018
    S2999 --> S3019
    S2999 --> S3020
    S2999 --> S3021
    S2999 --> S3022
    S2999 --> S3023
    S2999 --> S3024
    S2999 --> S3025
    S2999 --> S3026
    S2999 --> S3027
    S2999 --> S3028
    S2999 --> S3029
    S2999 --> S3030
    S2999 --> S3031
    S2999 --> S3032
    S2999 --> S3033
    S2999 --> S3034
    S2999 --> S3035
    S2999 --> S3036
    S2999 --> S3037
    S2999 --> S3038
    S2999 --> S3039
    S2999 --> S3040
    S2999 --> S3041
    S2999 --> S3042
    S2999 --> S3043
    S2999 --> S3044
    S2999 --> S3045
    S2999 --> S3046
    S2999 --> S3047
    S2999 --> S3048
    S2999 --> S3049
    S2999 --> S3050
    S2999 --> S3051
    S2999 --> S3052
    S2999 --> S3053
    S2999 --> S3054
    S2999 --> S3055
    S2999 --> S3056
    S2999 --> S3057
    S2999 --> S3058
    S2999 --> S3059
    S2999 --> S3060
    S2999 --> S3061
    S2999 --> S3062
    S2999 --> S3063
    S2999 --> S3064
    S2999 --> S3065
    S2999 --> S3066
    S2999 --> S3067
    S2999 --> S3068
    S2999 --> S3069
    S2999 --> S3070
    S2999 --> S3071
    S2999 --> S3072
    S2999 --> S3073
    S2999 --> S3074
    S2999 --> S3075
    S2999 --> S3076
    S2999 --> S3077
    S2999 --> S3078
    S2999 --> S3079
    S2999 --> S3080
    S2999 --> S3081
    S2999 --> S3082
    S2999 --> S3083
    S2999 --> S3084
    S2999 --> S3085
    S2999 --> S3086
    S2999 --> S3087
    S2999 --> S3088
    S2999 --> S3089
    S2999 --> S3090
    S2999 --> S3091
    S2999 --> S3092
    S2999 --> S3093
    S2999 --> S3094
    S2999 --> S3095
    S2999 --> S3096
    S2999 --> S3097
    S2999 --> S3098
    S2999 --> S3099
    S2999 --> S3100
    S3001 --> S3000
    S3002 --> S3000
    S3003 --> S3000
    S3004 --> S3000
    S3005 --> S3000
    S3006 --> S3000
    S3007 --> S3000
    S3008 --> S3000
    S3009 --> S3000
    S3010 --> S3000
    S3011 --> S3000
    S3012 --> S3000
    S3013 --> S3000
    S3014 --> S3000
    S3015 --> S3000
    S3016 --> S3000
    S3017 --> S3000
    S3018 --> S3000
    S3019 --> S3000
    S3020 --> S3000
    S3021 --> S3000
    S3022 --> S3000
    S3023 --> S3000
    S3024 --> S3000
    S3025 --> S3000
    S3026 --> S3000
    S3027 --> S3000
    S3028 --> S3000
    S3029 --> S3000
    S3030 --> S3000
    S3031 --> S3000
    S3032 --> S3000
    S3033 --> S3000
    S3034 --> S3000
    S3035 --> S3000
    S3036 --> S3000
    S3037 --> S3000
    S3038 --> S2999
    S3039 --> S3000
    S3040 --> S3000
    S3041 --> S3000
    S3042 --> S3000
    S3043 --> S3000
    S3044 --> S3000
    S3045 --> S3000
    S3046 --> S3000
    S3047 --> S3000
    S3048 --> S3000
    S3049 --> S3000
    S3050 --> S3000
    S3051 --> S3000
    S3052 --> S3000
    S3053 --> S3000
    S3054 --> S2999
    S3055 --> S3000
    S3056 --> S3000
    S3057 --> S3000
    S3058 --> S3000
    S3059 --> S3000
    S3060 --> S3000
    S3061 --> S3000
    S3062 --> S3000
    S3063 --> S3000
    S3064 --> S3000
    S3065 --> S3000
    S3066 --> S3000
    S3068 --> S3069
    S3069 --> S3000
    S3071 --> S3000
    S3072 --> S3000
    S3073 --> S3000
    S3074 --> S3000
    S3075 --> S3000
    S3076 --> S3000
    S3077 --> S3000
    S3079 --> S3000
    S3080 --> S3000
    S3082 --> S3000
    S3083 --> S3000
    S3084 --> S3000
    S3085 --> S3000
    S3086 --> S3000
    S3087 --> S3000
    S3088 --> S3000
    S3089 --> S3000
    S3090 --> S3000
    S3091 --> S3000
    S3092 --> S3000
    S3093 --> S3000
    S3094 --> S3000
    S3095 --> S3000
    S3096 --> S3000
    S3097 --> S3000
    S3098 --> S3000
    S3099 --> S3000
    S3100 --> S3000
    S3500 --> S3500
    S3500 --> S3600
    S3500 --> S4000
    S3500 --> S4001
    S3600 --> S3600
    S3600 --> S3700
    S3600 --> S3800
    S3600 --> S3900
    S3600 --> S3950
    S3600 --> S3975
    S3600 --> S4000
    S3600 --> S4001
    S3700 --> S3600
    S3800 --> S3600
    S3800 --> S4001
    S3900 --> S3600
    S3950 --> S3600
    S3975 --> S4000
    S3976 --> S3990
    S3977 --> S3990
    S3978 --> S3989
    S3978 --> S3990
    S3979 --> S3990
    S3980 --> S3989
    S3980 --> S3990
    S4000 --> S4001
    S9999 --> S9998
    S9999 --> S9999
    S9999 --> S10000
    S10000 --> S39760
    S10000 --> S39770
    S10000 --> S39780
    S10000 --> S39790
    S10000 --> S39800
    S10000 --> S39900
    S10000_1 --> S3976
    S10000_1 --> S3977
    S10000_1 --> S3978
    S10000_1 --> S3979
    S10000_1 --> S3980
    S10000_1 --> S3990
    S10000_15 --> S10000_1
    S10000_15 --> S10000_15
    S10100 --> S1020
    S10110 --> S1020
    S10110 --> S102000
    S19999_9 --> S9900
    S19999_9 --> S19999_9
    S35000 --> S35000
    S35000 --> S36000
    S35000 --> S40000
    S36000 --> S35000
    S36000 --> S36000
    S36000 --> S37000
    S36000 --> S38000
    S36000 --> S39000
    S36000 --> S39500
    S36000 --> S39750
    S36000 --> S40000
    S37000 --> S36000
    S38000 --> S36000
    S39000 --> S36000
    S39500 --> S36000
    S39750 --> S40000
    S39760 --> S39900
    S39770 --> S39890
    S39770 --> S39900
    S39780 --> S39890
    S39780 --> S39900
    S39790 --> S39900
    S39800 --> S39890
    S39800 --> S39900
    S99998 --> S99998
    S99998 --> S100000
    S99999 --> S99999
    S99999 --> S100000
    S100000 --> S100002
    S102000 --> S102001
    S1000005 --> S1000000
    S1000005 --> S1000005
```

**Statistics:**
- Total States: 362
- Total Transitions: 742
- Categories: 13

**State Categories:**
- BattleAdv: 10 states
- BattleBasic: 4 states
- CharCreation: 23 states
- Encampment: 74 states
- Level1: 41 states
- Level2_3: 41 states
- MagicBoss: 115 states
- Menu: 8 states
- NecroBattle: 14 states
- NecroFight: 2 states
- Other: 14 states
- SaveLoad: 8 states
- Shop: 8 states
