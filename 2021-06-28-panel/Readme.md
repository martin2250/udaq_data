python -m taxi_hal udaq_power off --channel 0-7
python -m taxi_hal udaq_power on --channel 1
cd ~/daq/udaq/scripts && ./configure_MicroDAQ_005_histogram_fwd_1000.sh 1

# measurements without led
cd ~/daq/udaq/scripts; ./run_MicroDAQ_003_100s.sh 1 ; ./save_MicroDAQ_002_histogram_Tim.sh 1

# measurements with led
cd ~/daq/udaq/scripts; ./run_MicroDAQ_003_20seconds.sh 1 ; ./save_MicroDAQ_002_histogram_Tim.sh 1

# runs
## 03
pulser: -2 to 2 volts, 500us burst
AUXDAC 2650
## 04
pulser -2 to 3 volts, 500us burst
## 05
pulser -2 to 3 volts, 2ms burst
## 06
pulser -2 to 4 volts, 2ms burst
## 07
new led position
pulser -2 to 5 volts, 500us burst
## 08
led position same as with icearm measurements
pulser -2 to 5 volts, 500us burst

## 09 
same as 8, with AUXDAC at 2820