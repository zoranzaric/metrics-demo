# metrics-demo
This is a project to demonstrate the problem that the open-telemetry-javaagen prometheus metrics exporter does not export the same metrics as the spring-boot actuator prometheus exporter.

## OTEL Exporter
```
# HELP queueSize The number of spans queued
# HELP runtime_jvm_gc_count_total The number of collections that have occurred for a given JVM garbage collector.
# HELP runtime_jvm_gc_time_total Time spent in a given JVM garbage collector in milliseconds.
# HELP runtime_jvm_memory_area Bytes of a given JVM memory area.
# HELP runtime_jvm_memory_pool Bytes of a given JVM memory pool.
```

## spring-boot
```
# HELP application_ready_time_seconds Time taken (ms) for the application to be ready to service requests
# HELP application_started_time_seconds Time taken (ms) to start the application
# HELP disk_free_bytes Usable space for path
# HELP disk_total_bytes Total space for path
# HELP executor_active_threads The approximate number of threads that are actively executing tasks
# HELP executor_completed_tasks_total The approximate total number of tasks that have completed execution
# HELP executor_pool_core_threads The core number of threads for the pool
# HELP executor_pool_max_threads The maximum allowed number of threads in the pool
# HELP executor_pool_size_threads The current number of threads in the pool
# HELP executor_queue_remaining_tasks The number of additional elements that this queue can ideally accept without blocking
# HELP executor_queued_tasks The approximate number of tasks that are queued for execution
# HELP http_server_requests_seconds  
# HELP http_server_requests_seconds_max  
# HELP jvm_buffer_count_buffers An estimate of the number of buffers in the pool
# HELP jvm_buffer_memory_used_bytes An estimate of the memory that the Java virtual machine is using for this buffer pool
# HELP jvm_buffer_total_capacity_bytes An estimate of the total capacity of the buffers in this pool
# HELP jvm_classes_loaded_classes The number of classes that are currently loaded in the Java virtual machine
# HELP jvm_classes_unloaded_classes_total The total number of classes unloaded since the Java virtual machine has started execution
# HELP jvm_gc_live_data_size_bytes Size of long-lived heap memory pool after reclamation
# HELP jvm_gc_max_data_size_bytes Max size of long-lived heap memory pool
# HELP jvm_gc_memory_allocated_bytes_total Incremented for an increase in the size of the (young) heap memory pool after one GC to before the next
# HELP jvm_gc_memory_promoted_bytes_total Count of positive increases in the size of the old generation memory pool before GC to after GC
# HELP jvm_gc_overhead_percent An approximation of the percent of CPU time used by GC activities over the last lookback period or since monitoring began, whichever is shorter, in the range [0..1]
# HELP jvm_gc_pause_seconds Time spent in GC pause
# HELP jvm_gc_pause_seconds_max Time spent in GC pause
# HELP jvm_memory_committed_bytes The amount of memory in bytes that is committed for the Java virtual machine to use
# HELP jvm_memory_max_bytes The maximum amount of memory in bytes that can be used for memory management
# HELP jvm_memory_usage_after_gc_percent The percentage of long-lived heap pool used after the last GC event, in the range [0..1]
# HELP jvm_memory_used_bytes The amount of used memory
# HELP jvm_threads_daemon_threads The current number of live daemon threads
# HELP jvm_threads_live_threads The current number of live threads including both daemon and non-daemon threads
# HELP jvm_threads_peak_threads The peak live thread count since the Java virtual machine started or peak was reset
# HELP jvm_threads_states_threads The current number of threads having NEW state
# HELP logback_events_total Number of error level events that made it to the logs
# HELP process_cpu_usage The "recent cpu usage" for the Java Virtual Machine process
# HELP process_files_max_files The maximum file descriptor count
# HELP process_files_open_files The open file descriptor count
# HELP process_start_time_seconds Start time of the process since unix epoch.
# HELP process_uptime_seconds The uptime of the Java virtual machine
# HELP system_cpu_count The number of processors available to the Java virtual machine
# HELP system_cpu_usage The "recent cpu usage" of the system the application is running in
# HELP system_load_average_1m The sum of the number of runnable entities queued to available processors and the number of runnable entities running on the available processors averaged over a period of time
# HELP tomcat_sessions_active_current_sessions  
# HELP tomcat_sessions_active_max_sessions  
# HELP tomcat_sessions_alive_max_seconds  
# HELP tomcat_sessions_created_sessions_total  
# HELP tomcat_sessions_expired_sessions_total  
# HELP tomcat_sessions_rejected_sessions_total  
```
