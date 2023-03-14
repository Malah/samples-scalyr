Use third party monitor with Dataset Agent

0.  install agent; configure agent; start agent
1.  git clone https://github.com/scalyr/samples.git
2.  cp samples/monitors/log_gen.py /usr/share/scalyr-agent-2/py/scalyr_agent/builtin_monitors
```
   monitors: [
    {
            "module": "scalyr_agent.builtin_monitors.log_gen",
            "logs": "/tmp/logs/*",
            "type_array":"['cisco', 'windows_dns']",
            "parser":"json",
            "time_pattern":"(?P<date>(\\d+ \\w+ \\d+|\\d+\\/\\d+\\/\\d+)) (?P<time>(\\d{2}:\\d{2}:\\d{2}\\.\\d{3}|\\d+:\\d+:\\d+ \\w+))",
            "sampling_rate":".2"}

   ]
 ```
