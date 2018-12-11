# Vaja9-DAC-STM32VL
DAC pretvorba
-----------------------------------
ODGOVORI:
2. b.) 2 izhoda.
c.) od 0V do 3.3V.
d.) PA4.
e.) Output buffer, Trigger.
3. b.)&hdac
---------------------------------
KOMENTAR NA DELOVANJE:
V User code begin 2 sva morala spremeniti vrstni red spremenljivk tako da sva jih zamenjala:
valByte = (uint8_t)((valVolt/3.0)*255);
HAL_DAC_Start(&hdac,DAC_CHANNEL_1);
HAL_DAC_SetValue(&hdac, DAC_CHANNEL_1, DAC_ALIGN_8B_R, valByte);
Najprej je kazalo napetost 1.54V, po spremembi pa 2.19V. 
