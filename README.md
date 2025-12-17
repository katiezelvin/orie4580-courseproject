# orie4580-courseproject

The file "simulation.py" contains code to run a baseline simulation, with batching or will chunked prefill.
The file "main_report.pdf" contains a summary report of main findings and a technical appendix

**Explanation of simulation.py**
To run simulation for baseline or batching use run_simulation(arrival_rate, total_queries, verbose, warmup_time, analysis_time, mode)
arrival_rate = queries per second to arrive, it is an exponential distribution
total_queries = how many requests/queries the simulation should run for
verbose = True if printed metrics, false otherwise
warmuptime = Time in seconds to start observing metrics
analysistime = Time in seconds to let elapse after warmup time complete
mode = "batch" or "fcfs", "batch" is decode-priortizing with some batching, "fcfs" is a baseline first-come, first-serve model
num_gpus = integer number describing the amount of GPUs or servers you decide to run you simulation with

The output is: average queries in system, throughput (queries per second), time between tokens (TBT), 95th percentile TBT, time to first token (TTFT), 95th percentile TTFT

To run simulation for chunk prefill use:
run_chunk_experiment(chunk_size, arrival_rate, total_queries)

chunk_size: maximum number of prefill tokens from one query processed in a batch
arrival_rate: queries per second to arrive, exponential distribution
total_queries: how many queries to run simulation for



