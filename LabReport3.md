# Command Options for 'find'

## Option 1: -name

- Example 1:

The command
```
find -name Algarve-History.txt
```
yields
```
./travel_guides/berlitz2/Algarve-History.txt
```
- Example 2:

The command
```
find -name "chM.txt"
```
yields
```
./non-fiction/OUP/Castro/chM.txt
```
## Option 2: -iname

- Example 1:

The command
```
find -iname chm.txt
```
yields
```
./non-fiction/OUP/Castro/chM.txt
```

- Example 2:

The command
```
find -iname handrisrael.txt
```
Yields
```
./travel_guides/berlitz1/HandRIsrael.txt
```
