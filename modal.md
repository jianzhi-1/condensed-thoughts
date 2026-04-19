# Modal

```shell
modal setup
modal --version
```

Volume

```shell
modal volume create <name>
modal volume put <name> ./mount-dir .
```

Cold-start time. Container can be warm and hence 0 cold-start time.

Function call

Images


Cancel

fc-01KPJ3A90FM386Z0B2R9QGTX5S

Copy Function call ID
Input ID:
in-01KPJ3A91C01CVK1YZXBJKX4K1


Resources
Autoscaling (min, max, buffer containers) - what's scaledown window?

Storage - type: volume, mount path

Container:
ta-01KPJ3AAQ0JQZPC2BV5NPTD050
B200

Region and cloud based scheduling

```
Running benchmark on Modal B200...
Task's current input(s) ["in-01KPJ3A91C01CVK1YZXBJKX4K1:1776576439351-0"] cancelled because: Task's current input in-01KPJ3A91C01CVK1YZXBJKX4K1:1776576439351-0 hit its timeout of 3600s
[modal-client] 2026-04-19T06:27:26+0000 Received a cancellation signal while processing input ('in-01KPJ3A91C01CVK1YZXBJKX4K1:1776576439351-0',)
Stopping app - uncaught exception raised locally: FunctionTimeoutError("Task's current input in-01KPJ3A91C01CVK1YZXBJKX4K1:1776576439351-0 hit its timeout of 3600s").
Stopping app - uncaught exception raised locally: FunctionTimeoutError("Task's current input in-01KPJ3A91C01CVK1YZXBJKX4K1:1776576439351-0 hit its timeout of 3600s").
[modal-client] 2026-04-19T06:27:28+0000 Successfully canceled input ('in-01KPJ3A91C01CVK1YZXBJKX4K1:1776576439351-0',)
/usr/local/lib/python3.12/multiprocessing/resource_tracker.py:279: UserWarning: resource_tracker: There appear to be 1 leaked semaphore objects to clean up at shutdown
  warnings.warn('resource_tracker: There appear to be %d '
[W419 06:27:29.368035213 CudaIPCTypes.cpp:16] Producer process has been terminated before all shared CUDA tensors released. See Note [Sharing CUDA tensors]
╭─────────────────────────────── Traceback (most recent call last) ────────────────────────────────╮
│ /Users/jianzhichicago/nv-gated-delta-net/scripts/run_modal.py:118 in main                        │
│                                                                                                  │
│   117 │   print("\nRunning benchmark on Modal B200...")                                          │
│ ❱ 118 │   results = run_benchmark.remote(solution)                                               │
│   119                                                                                            │
│                                                                                                  │
│ /Users/jianzhichicago/miniforge3/envs/fi-bench/lib/python3.12/site-packages/modal/_object.py:46  │
│ in wrapped                                                                                       │
│                                                                                                  │
│    45 │   │   await self.hydrate()                                                               │
│ ❱  46 │   │   return await method(self, *args, **kwargs)                                         │
│    47                                                                                            │
│                                                                                                  │
│ /Users/jianzhichicago/miniforge3/envs/fi-bench/lib/python3.12/site-packages/modal/_functions.py: │
│ 1702 in remote                                                                                   │
│                                                                                                  │
│   1701 │   │                                                                                     │
│ ❱ 1702 │   │   return await self._call_function(args, kwargs)                                    │
│   1703                                                                                           │
│                                                                                                  │
│ /Users/jianzhichicago/miniforge3/envs/fi-bench/lib/python3.12/site-packages/modal/_functions.py: │
│ 1646 in _call_function                                                                           │
│                                                                                                  │
│   1645 │   │                                                                                     │
│ ❱ 1646 │   │   return await invocation.run_function()                                            │
│   1647                                                                                           │
│                                                                                                  │
│ /Users/jianzhichicago/miniforge3/envs/fi-bench/lib/python3.12/site-packages/modal/_functions.py: │
│ 291 in run_function                                                                              │
│                                                                                                  │
│    290 │   │   │   item = await self._get_single_output()                                        │
│ ❱  291 │   │   │   return await _process_result(item.result, item.data_format, self.stub, self.  │
│    292                                                                                           │
│                                                                                                  │
│ /Users/jianzhichicago/miniforge3/envs/fi-bench/lib/python3.12/site-packages/modal/_utils/functio │
│ n_utils.py:489 in _process_result                                                                │
│                                                                                                  │
│   488 │   if result.status == api_pb2.GenericResult.GENERIC_STATUS_TIMEOUT:                      │
│ ❱ 489 │   │   raise FunctionTimeoutError(result.exception)                                       │
│   490 │   elif result.status == api_pb2.GenericResult.GENERIC_STATUS_INTERNAL_FAILURE:           │
╰──────────────────────────────────────────────────────────────────────────────────────────────────╯
FunctionTimeoutError: Task's current input in-01KPJ3A91C01CVK1YZXBJKX4K1:1776576439351-0 hit its timeout of 3600s
```
