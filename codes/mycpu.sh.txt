#!/bin/sh
cpt=$(sysctl -n dev.cpu.0.temperature | sed 's/\.[^>]*C//g')
if [ $cpt -ge 50 ]
then
echo "<txt><span weight='bold' fgcolor='red'>$cpo C</span></txt>"
else
echo "<txt><span weight='bold' fgcolor='white'>$cpt C</span></txt>"
fi
