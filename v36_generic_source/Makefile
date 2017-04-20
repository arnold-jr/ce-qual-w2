FIRST = w2modules.f90 w2_36_gen.f90 input.f90
SRCS := $(wildcard *.f90)
SRCS := $(FIRST) $(filter-out $(FIRST), $(SRCS))
OBJS := $(SRCS:.f90=.o)

FFLAGS = -O3 -real_size 64 -Bstatic -threads -openmp 
fcompiler = ifort 

%.o: %.f90
	$(fcompiler) $(FFLAGS) -c $< -o $@

cequalw2: $(OBJS) 
	$(fcompiler) $(FFLAGS) -o $@ $^

clean:
	rm *.o

#cequalw2: $(OBJS)
#	$(fcompiler) $(FFLAGS) -o cequalw2 $(objects)
#w2modules.o: w2modules.f90
#	$(fcompiler) $(FFLAGS) w2modules.f90
#w2_36_gen.o: w2_36_gen.f90
#	$(fcompiler) $(FFLAGS) w2_36_gen.f90
#input.o: input.f90
#	$(fcompiler) $(FFLAGS) input.f90
#az.o: az.f90
#	$(fcompiler) $(FFLAGS) az.f90
#balances.o: balances.f90
#	$(fcompiler) $(FFLAGS) balances.f90
#date.o: date.f90
#	$(fcompiler) $(FFLAGS) date.f90
#density.o: density.f90
#	$(fcompiler) $(FFLAGS) density.f90
#endsimulation.o: endsimulation.f90
#	$(fcompiler) $(FFLAGS) endsimulation.f90
#gas-transfer.o: gas-transfer.f90
#	$(fcompiler) $(FFLAGS) gas-transfer.f90
#gate-spill-pipe.o: gate-spill-pipe.f90
#	$(fcompiler) $(FFLAGS) gate-spill-pipe.f90
#heat-exchange.o: heat-exchange.f90
#	$(fcompiler) $(FFLAGS) heat-exchange.f90
#hydroinout.o: hydroinout.f90
#	$(fcompiler) $(FFLAGS) hydroinout.f90
#init-cond.o: init-cond.f90
#	$(fcompiler) $(FFLAGS) init-cond.f90
#init-geom.o: init-geom.f90
#	$(fcompiler) $(FFLAGS) init-geom.f90
#init.o: init.f90
#	$(fcompiler) $(FFLAGS) init.f90
#layeraddsub.o: layeraddsub.f90
#	$(fcompiler) $(FFLAGS) layeraddsub.f90
#macrophyte-aux.o: macrophyte-aux.f90
#	$(fcompiler) $(FFLAGS) macrophyte-aux.f90
#output.o: output.f90
#	$(fcompiler) $(FFLAGS) output.f90
#outputa.o: outputa.f90
#	$(fcompiler) $(FFLAGS) outputa.f90
#outputinit.o: outputinit.f90
#	$(fcompiler) $(FFLAGS) outputinit.f90
#restart.o: restart.f90
#	$(fcompiler) $(FFLAGS) restart.f90
#shading.o: shading.f90
#	$(fcompiler) $(FFLAGS) shading.f90
#tdg.o: tdg.f90
#	$(fcompiler) $(FFLAGS) tdg.f90
#temperature.o: temperature.f90
#	$(fcompiler) $(FFLAGS) temperature.f90
#time-varying-data.o: time-varying-data.f90
#	$(fcompiler) $(FFLAGS) time-varying-data.f90
#transport.o: transport.f90
#	$(fcompiler) $(FFLAGS) transport.f90
#update.o: update.f90
#	$(fcompiler) $(FFLAGS) update.f90
#water-quality.o: water-quality.f90
#	$(fcompiler) $(FFLAGS) water-quality.f90
#waterbody.o: waterbody.f90
#	$(fcompiler) $(FFLAGS) waterbody.f90
#withdrawal.o: withdrawal.f90
#	$(fcompiler) $(FFLAGS) withdrawal.f90
#wqconstituents.o: wqconstituents.f90
#	$(fcompiler) $(FFLAGS) wqconstituents.f90
