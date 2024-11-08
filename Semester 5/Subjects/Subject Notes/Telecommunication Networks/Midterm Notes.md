# Python
## JSON 
`json.load(read_file)` -> dictionary-t ad vissza
`json.dump(data,write_file)` -> dictionary JSON-né alakítása és mentése

## Struct
`packer = struct.Struct()`
`packer.unpack()` és `packer.pack()`

## Fájl kezelés
`seek(offset,whence)`, ahol:
- `offset` - mutató pozíciója
- `whence`:
	- 0: abszolút
	- 1: relatív
	- 2: fájl végétől 

## Socket
`socket.send()` vs. `socket.sendall()` -> utóbbi vagy "exception"-t dob, vagy az összes kért adatot átküldi több `send` parancs segítségével; nem lehet tudni, hogy mennyi byte-ot küldött át

`setblocking()` és `settimeout()`
- `setblocking(1)` - várunk ameddig el nem végezhető lesz a művelet
- `setblocking(0)` - azonnal dobjunk kivételt, ha nem végezhető el
- `setblocking(0<)` - egy idő után dobjunk kivételt, ha nem  végezhető el a művelet