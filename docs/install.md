# installation

## via Raspberry pi imager

## activer le ssh sur /boot

```
touch boot/ssh
```

## ssh dans le raspberry 
* set password
* set hostname
* vnc 
* update 
* upgrade


## Nom 
* cm-pi-be-1.local

## Poe Fan Curve

`/boot/config.txt`

```
# PoE Hat Fan Speeds
dtparam=poe_fan_temp0=50000
dtparam=poe_fan_temp1=60000
dtparam=poe_fan_temp2=70000
dtparam=poe_fan_temp3=80000
```

