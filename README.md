# IGSPORT BSC300 Map Creator

This repository provides tools to generate map files compatible with the IGSPORT BSC300 device using data from OpenStreetMap.

It is based on the description by CYMES [source](https://www.pepper.pl/dyskusji/igpsport-bsc300-informacje-o-mapach-1046955?page=2#comments).

## Usage

Run the tool with the following syntax:

```bash
./generate_map.sh -i input_map_file.pbf -o output_map_filename
```

* Input map files can be downloaded from [Geofabrik](https://download.geofabrik.de/).
* The output will be a `.map` file, automatically generated with the correct extension.
* The output filename must follow a specific format to be recognized by BSC300 firmware.

### Output Filename Format

The filename should include:

* **Country code**
* **4-digit map version number**
* **Date** in the format `YYMMDD`
* **Additional characters**, which are device-specific and must match expected patterns (currently unknown but required). Use the examples below as templates.

**Example:** `-o PL00002507043EJ20506N068` (for Poland)

### Example Filenames by Country
| Country             | Example Filename             |
| ------------------- | ---------------------------- |
|Argentina 🇦🇷 | AR00002503171UZ3JT0DA0RX.map|
|Australia 🇦🇺 | AU00002503174FN3BK1OB105.map|
|Austria 🇦🇹 | AT00001111113BR26204W02L.map|
|Bosnia and Herzegovina 🇧🇦 | BA00002503313FO29J02J02H.map|
|Bahrain 🇧🇭 | GC00002503173RK2JU0G10BL.map|
|Belarus 🇧🇾 | BY00002408073JS1YF06R066.map|
|Belgium 🇧🇪 | BE000025031737923N02L022.map|
|Bolivia 🇧🇴 | BO00002503281XI3BT07Z09C.map|
|Brazil 🇧🇷 | BR00002503251UO32A0SV0QB.map|
|Malaysia 🇲🇾 | MY00002503254WR3100CF04I.map|
|Bulgaria 🇧🇬 | BG00002407153JK29V04B03C.map|
|Cambodia 🇰🇭 | KH00002503174YE2VY03N03J.map|
|Canada 🇨🇦 | CA00002311170EV08Z25I48I.map|
|Spain 🇪🇸 | ES35001111112UA2LH03R024.map|
|Chile 🇨🇱 | CL000025031718L3GW0R80WF.map|
|China 🇨🇳 | CN00002503204G32141330UK.map|
|Colombia 🇨🇴 | CO00002503171Q12VL0AS0CY.map|
|Croatia 🇭🇷 | HR00002503173EA28C03T03T.map|
|Cyprus 🇨🇾 | CY00002408273Q62HK01H00W.map|
|Czech Republic 🇨🇿 | CZ00002503173DD24304C02J.map|
|Denmark 🇩🇰 | DK00002503173AV1WT04I03N.map|
|Ecuador 🇪🇨 | EC00002503171JM34P0AR04A.map|
|Egypt 🇪🇬 | EG00002501033KQ2KL08L08G.map|
|Finland 🇫🇮 | FI00002311173GN1E00940GP.map|
|France 🇫🇷 | FR000025031732I23V09I096.map|
|Georgia 🇬🇪 | GE00002503173V02AR04C02K.map|
|Germany 🇩🇪 | DE000025031739H1ZQ05Z083.map|
|Greece 🇬🇷 | GR00002502103I02CN06I05N.map|
|Guyana 🇬🇾 | GY000025031722W30B03I04W.map|
|Hungary 🇭🇺 | HU00002503173FY26904I032.map|
|India 🇮🇳 | IN00002503174CK2HO0JC0JT.map|
|Indonesia 🇮🇩 | ID00002503174TT31X0TL0AV.map|
|Ireland 🇮🇪 | IE00002406252Z01YM032056.map|
|Israel 🇮🇱 | IL00001111113QT2J901T03O.map|
|Italy 🇮🇹 | IT000025031739Y27S07J09Z.map|
|Japan 🇯🇵 | JP00002503175BH29D0JN0J8.map|
|Kazakhstan 🇰🇿 | KZ00002503313Z11ZA0Q10HM.map|
|Kuwait 🇰🇼 | GC00002503173RK2JU0G10BL.map|
|Kyrgyzstan 🇰🇬 | KG00002503314DJ2BA06X03J.map|
|Lithuania 🇱🇹 | LT00002502103IZ1Y503U034.map|
|Luxembourg 🇱🇺 | LU000025031739D24Y00K00S.map|
|Malaysia 🇲🇾 | MY00002503254WR3100CF04I.map|
|Montenegro 🇲🇪 | ME00002503313HE2B201A01J.map|
|Mexico 🇲🇽 | MX000025032512Y2JU0K00CN.map|
|North Macedonia 🇲🇰 | MK000025041007X059004003.map|
|North Macedonia 🇲🇰 | MK00002504103IO2C201V01G.map|
|Morocco 🇲🇦 | MA00002311262UY2GM0A70BQ.map|
|Myanmar 🇲🇲 | MM00002503174S02MX05R0CR.map|
|Netherlands 🇳🇱 | AN000025031737T21J02J02Z.map|
|Norway 🇳🇴 | NO00002311172X90ME0U61B6.map|
|New Zealand 🇳🇿 | NZ000025021000Q3P46A80JX.map|
|Oman 🇴🇲 | GC00002503173RK2JU0G10BL.map|
|Paraguay 🇵🇾 | PY000025031721Y3I005L068.map|
|Peru 🇵🇪 | PE00002503171QD35G08B0C6.map|
|Philippines 🇵🇭 | PH000025031754P2S40930AR.map|
|Poland 🇵🇱 | PL00002503173EJ20506N068.map|
|Portugal 🇵🇹 | PT00002503172M02C80FW07V.map|
|Qatar 🇶🇦 | GC00002503173RK2JU0G10BL.map|
|France 🇫🇷 | FR940024071744O3J900E00D.map|
|Romania 🇷🇴 | RO00002503173IH26U06404A.map|
|Saudi Arabia 🇸🇦 | GC00002503173RK2JU0G10BL.map|
|Serbia 🇷🇸 | RS00002412313HI28M03C03P.map|
|Singapore 🇸🇬 | MY00002503254WR3100CF04I.map|
|Slovakia 🇸🇰 | SK00002311173G525G042020.map|
|Slovenia 🇸🇮 | SI00002311173E528002701Q.map|
|South Korea 🇰🇷 | KR00002503205CJ2F804L04C.map|
|Spain 🇪🇸 | ES00002503182ZW2AX08M070.map|
|Suriname 🇸🇷 | SR000025031724L31Y03B039.map|
|Sweden 🇸🇪 | SE00002503173CP1GK08H0J1.map|
|Switzerland 🇨🇭 | CH000025031739G27903001Y.map|
|Tajikistan 🇹🇯 | TJ00002503314CB2D904X03L.map|
|Thailand 🇹🇭 | TH00002503174V42SE05J09V.map|
|Turkey 🇹🇷 | TR00002503173M02C50CG060.map|
|Turkmenistan 🇹🇲 | TM00002503313ZB2810CY0A7.map|
|Ukraine 🇺🇦 | UA00002503173JK22Q0BN07O.map|
|United Arab Emirates 🇦🇪 | GC00002503173RK2JU0G10BL.map|
|United Kingdom 🇬🇧 | UK00002503172X41SZ09S0CC.map|
|Uruguay 🇺🇾 | UY000025031724D3NK04606W.map|
|Uzbekistan 🇺🇿 | UZ000025033144F28M0BM086.map|
|Venezuela 🇻🇪 | VE00002503171VE2VQ08M0AE.map|
|Vietnam 🇻🇳 | VN00002503174Y22QK0800A7.map|
