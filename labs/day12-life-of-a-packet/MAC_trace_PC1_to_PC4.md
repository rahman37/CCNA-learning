# MAC Address Flow: PC1 to PC4

## A. PC1 → SW1
- **Source MAC:** PC1 (e.g., `1111`)
- **Destination MAC:** R1 G0/0 (`aaaa`)

## B. SW1 → R1
- Same as above

## C. R1 → R2
- **Source MAC:** R1 G0/1 (`bbbb`)
- **Destination MAC:** R2 G0/0 (`cccc`)

## D. R2 → R3
- **Source MAC:** R2 G0/1 (`dddd`)
- **Destination MAC:** R3 G0/0 (`eeee`)

## E. R3 → SW2
- **Source MAC:** R3 G0/1 (`ffff`)
- **Destination MAC:** PC4 (`4444`)

## F. SW2 → PC4
- Same as above
