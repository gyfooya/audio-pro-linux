# CPUPOWER systemd service

## Quick comparison (audio perspective)

| Governor     | Latency | Stability | Audio use |
|-------------|---------|-----------|-----------|
| performance | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ✅ Pro |
| schedutil   | ⭐⭐⭐     | ⭐⭐⭐     | ⚠️ Casual |
| ondemand    | ⭐⭐      | ⭐⭐      | ❌ Risky |
| powersave   | ⭐       | ⭐       | ❌ No |
<pre>
⚠️ Warning: Not all CPUs support all governors
CPU governor availability depends on:
 - CPU model
 - Kernel configuration
 - Active CPU frequency driver (intel_pstate, acpi-cpufreq, etc.)
Do not assume performance, schedutil, etc. are always available.

List available CPU governors
-cat /sys/devices/system/cpu/cpu0/cpufreq/scaling_available_governors
</pre>

# Archlinux Installation / Configuration
- sudo pacman -S linux-tools
- sudo nano /etc/default/cpupower

```
# Define CPUs governor
# valid governors: ondemand, performance, powersave, conservative, userspace.
governor="performance"

#governor="powersave"
#governor='ondemand'

# Limit frequency range
# Valid suffixes: Hz, kHz (default), MHz, GHz, THz
#min_freq="2.25GHz"
#max_freq="3GHz"

# Specific frequency to be set.
# Requires userspace governor to be available.
# Do not set governor field if you use this one.
#freq=

# Utilizes cores in one processor package/socket first before processes are
# scheduled to other processor packages/sockets.
# See man (1) CPUPOWER-SET for additional details.
#mc_scheduler=

# Utilizes thread siblings of one processor core first before processes are
# scheduled to other cores. See man (1) CPUPOWER-SET for additional details.
#smp_scheduler=

#  Sets a register on supported Intel processore which allows software to convey
# its policy for the relative importance of performance versus energy savings to
# the  processor. See man (1) CPUPOWER-SET for additional details.
#perf_bias=

#vim:set ts=2 sw=2 ft=sh et:
```


# Enable & Activate systemd service
- sudo systemctl enable --now cpupower.service

# Restart systemd service
- sudo systemctl restart cpupower.service

# View actual scaling governor
- cat /sys/devices/system/cpu/cpu0/cpufreq/scaling_governor
