#
# Process this file with automake to produce Makefile.in
#

SUBDIRS = cluster scalability_1 scalability_2 scalability_3 calendar datetime flow_alternate_1 flow_alternate_2 flow_fixed constraints_combined_1 constraints_combined_2 constraints_leadtime_1 constraints_leadtime_2 lpsolver_1 constraints_material_1 constraints_material_2 constraints_material_3 constraints_material_4 jobshop xml constraints_resource_1 constraints_resource_2 constraints_resource_3 constraints_resource_4 constraints_resource_5 constraints_resource_6 problems deletion operation_alternate operation_available operation_effective operation_pre_post operation_routing name multithreading sample_module callback pegging xml_remote python_1 python_2 python_3 demand_policy safety_stock buffer_procure_1 flow_effective load_alternate load_effective setup_1 setup_2 setup_3 skills wip

EXTRA_DIST = runtest.py

if LP
check:
	`pwd`/runtest.py ${TESTARGS}
else
check:
	`pwd`/runtest.py ${TESTARGS} -e lpsolver_1
endif
