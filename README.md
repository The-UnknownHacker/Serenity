# Serenity

**Serenity** is a drumpad or macropad designed with musicians in mind.  
Instead of using traditional switches or buttons, it uses a **copper layer on the PCB** to detect touch input.

Powered by an **ESP32-S3 devkit**, Serenity can store sound files on a **microSD card** and output audio through a **headphone jack**.

It features **2 configurable buttons** that let you switch between sound "layers" — allowing you to play many more sounds than just 8.  
For example, with 4 layers, you can trigger **32 unique sounds**.

---

I built **Serenity** after being inspired by those expensive drumpads used for triggering sound effects.  
They often cost a fortune, so I created **Serenity** to cost **under $50 USD**, without sacrificing creativity or functionality.
=======


Images

-------------
Schematic

<img width="949" alt="image" src="https://github.com/user-attachments/assets/f0fa78f5-53b1-498f-8a3f-eec6fd9c29d3" />

PCB

<img width="1018" alt="image" src="https://github.com/user-attachments/assets/8b5f3a00-5c01-4daf-8e28-fe59e48f2ca4" />

3D Model

<img width="1009" alt="image" src="https://github.com/user-attachments/assets/f55a5422-c217-496a-b82c-ea7efde0140d" />


BOM

| Designator | Footprint | Quantity | Value | LCSC Part # | Purchase Method | Est. Price (USD) |
|------------|-----------|----------|-------|-------------|-----------------|-------------------|
| C1 | 1812 | 1 | 100nf | https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_TDK_C342613.html | PCBA | $0.34 |
| J1 | microSD_HC_Molex_47219-2001 | 1 | Micro_SD_Card | https://lcsc.com/product-detail/SD-Card-Memory-Card-Connector_MOLEX-472192001_C164170.html | PCBA | $0.48 |
| J2 | HRO_PJ-320D-A | 1 | PJ-320D-A | https://lcsc.com/product-detail/_Korean-Hroparts-Elec-PJ-320D-4A_C95562.html | PCBA | $1.50* |
| SW1, SW2 | SW_PUSH-12mm_Wuerth-430476085716 | 2 | SW_Push | https://www.adafruit.com/product/1119?srsltid=AfmBOoqwRE8KhgtdWcEbSr0UxHVauoeQpAy56lpgwJ67pl_6lD0DS_sJ | Ordering Online | $2.50* |
| U1 | ESP32-S2-DevKitC-1 | 1 | ESP32-S3-DevKitC | https://www.aliexpress.com/item/1005006446406795.html?src=google&pdp_npi=4%40dis!AUD!26.47!8.19!!!!!%40!12000037200113934!ppc!!!&snpsid=1&snps=y&src=google&albch=shopping&acnt=708-803-3821&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&gclsrc=aw.ds&&albagn=888888&&ds_e_adid=&ds_e_matchtype=&ds_e_device=c&ds_e_network=x&ds_e_product_group_id=&ds_e_product_id=en1005006446406795&ds_e_product_merchant_id=5551326180&ds_e_product_country=AU&ds_e_product_language=en&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=19366639602&albag=&isSmbAutoCall=false&needSmbHouyi=false&gad_source=1&gad_campaignid=17338734196&gbraid=0AAAAAD6I-hFKAadTE4Avff5KRQWZAVIR1&gclid=Cj0KCQjwmqPDBhCAARIsADorxIYCUFoJhmIURqGGyT1Bnp1HNg7o4UZPdnUgz-yrKNdseuVaICe9NbkaAqTaEALw_wcB | Ordering Online | $10.00 |
| U2 | TQFN-16-1EP_3x3mm_P0.5mm_EP1.23x1.23mm | 1 | MAX98357A | https://lcsc.com/product-detail/Audio-Amplifiers_Analog-Devices-Inc-Maxim-Integrated-MAX98357AETE-T_C910544.html?s_z=n_MAX98357AETE%2BT | PCBA | $3.50* |

## Total Estimated Cost
**Subtotal: ~$35 USD** without shipping

- Prices dont include shipping, taxes, and PCBA assembly fees
- PCBA components might have additional assembly costs
