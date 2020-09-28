# core_usage

The little GUI to show the usage of all cores.

## Compile

```bash
g++ -O2 -o core_usage core_usage.cpp -lX11 -lncurses
```

## Run

```bash
./core_usage [<int>] [txt]
```

The parameter <int> is the time interval of updating core utilization data
and the unit is second. Without it, 1.0 is used as default.
Parameter "txt" forces core_usage to run in console version although X11 is available.

The GUI will show up if X11 is available. If not, the console version will run.
If you want to run the console version even you have X11:

```bash
./core_usage 1.0 txt
```

## Log

In case you want to save core usage info into log file, you can:

```bash
export LOG_CORE_USAGE=1
```

before running core_usage.

Screen snapshot of GUI
![Alt text](core_usage_skx_gui.png?raw=true "Screen snapshot of GUI")

Screen snapshot of the terminal version
![Alt text](core_usage_ter.png?raw=true "Screen snapshot of terminal version")
