PLOT := ../udaq_plot/udaq_plot_hist.py

.PHONY:all
all: plots/led_pulses_med.pdf plots/light_tightness.pdf

plots:
	mkdir plots

plots/light_tightness.pdf: plots $(PLOT)
	$(PLOT) --title "2017 panel - light leaks?" --adcs h unmodified:01-unmodified-100s "after inserting LED:02-led-inside-100s-off" --save $@

plots/led_pulses_med.pdf: plots $(PLOT)
	$(PLOT) --title "2017 panel - LED pulses" --adcs m 07* --size 300,200 --save $@
