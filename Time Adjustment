#File : Time_Adjustment.ps1
#Prompt the user to convert Celsius in to Fahrenhet
#
$yclockin = read-host "Clockin"
$yclockinsplit = ($yclockin).split(":")
$yclockinsplit[0] = [Double]$yclockinsplit[0]
$yclockinsplit[1] = [Double]$yclockinsplit[1]
$yclockout = read-host "Clockout"
$yclockoutsplit = ($yclockout).split(":")
$yclockoutsplit[0] = [Double]$yclockoutsplit[0]
$yclockoutsplit[1] = [Double]$yclockoutsplit[1]
$yoffset1 = read-host "Type 1 or 0"
$yoffset1 = [Double]$yoffset1
$yoffset2 = read-host "Type .60 or 0"
$yoffset2 = [Double]$yoffset2
$ydecimal1 = $yclockoutsplit[1]/100
$ydecimal1 = [Double]$ydecimal1
$ydecimal2 = $yclockinsplit[1]/100
$ydecimal2 = [Double]$ydecimal2
$yd1 = ($yoffset2 + $ydecimal1 - $ydecimal2)/.60
$yd1 = [Double]$yd1
$yd2 = $yclockoutsplit[0] - $yclockinsplit[0] - $yoffset1
$yd2 = [Double]$yd2
$ydt = $yd1 + $yd2
$ydt = [Double]$ydt
$clockin = read-host "Clockin"
$clockinsplit = ($clockin).split(":")
$clockinsplit[0] = [Double]$clockinsplit[0]
$clockinsplit[1] = [Double]$clockinsplit[1]
$lunchin = read-host "Lunchin"
$lunchinsplit = ($lunchin).split(":")
$lunchinsplit[0] = [Double]$lunchinsplit[0]
$lunchinsplit[1] = [Double]$lunchinsplit[1]
$offset1 = read-host "Type 1 or 0"
$offset1 = [Double]$offset1
$offset2 = read-host "Type .60 or 0"
$offset2 = [Double]$offset2
$lunchout = read-host "Lunchout"
$lunchoutsplit = ($lunchout).split(":")
$lunchoutsplit[0] = [Double]$lunchoutsplit[0]
$lunchoutsplit[1] = [Double]$lunchoutsplit[1]
$clockout = read-host "Clockout"
$clockoutsplit = ($clockout).split(":")
$clockoutsplit[0] = [Double]$clockoutsplit[0]
$clockoutsplit[1] = [Double]$clockoutsplit[1]
$offset3 = read-host "Type 1 or 0"
$offset3 = [Double]$offset3
$offset4 = read-host "Type .60 or 0"
$offset4 = [Double]$offset4
$decimal1 = $lunchinsplit[1]/100
$decimal1 = [Double]$decimal1
$decimal2 = $clockinsplit[1]/100
$decimal2 = [Double]$decimal2
$firstd1 = ($offset2 + $decimal1 - $decimal2)/.60
$firstd1 = [Double]$firstd1
$firstd2 = $lunchinsplit[0] - $clockinsplit[0] - $offset1
$firstd2 = [Double]$firstd2
$firstdt = $firstd1 + $firstd2
$firstdt = [Double]$firstdt
Write-Host ""
$decimal3 = $clockoutsplit[1]/100
$decimal3 = [Double]$decimal3
$decimal4 = $lunchoutsplit[1]/100
$decimal4 = [Double]$decimal4
$secondd1 = ($offset4 + $decimal3 - $decimal4)/.60
$secondd1 = [Double]$secondd1
$secondd2 = $clockoutsplit[0] - $lunchoutsplit[0] - $offset3
$secondd2 = [Double]$secondd2
$seconddt = $secondd1 + $secondd2
$seconddt = [Double]$seconddt
$dt = $firstdt + $seconddt
$dt = [Double]$dt
$t = $dt + $ydt
$t = [Double]$t
Write-Host ""
Write-Host "Total Hours Worked"
$t
$timeremaining = 8 - $t
$timeremaining = [Double]$timeremaining
Write-Host "Time Remaining positive or negative"
$timeremaining
$timeremainingminutes = $timeremaining - [Math]::truncate($timeremaining)
$timeremainingminutes = [Double]$timeremainingminutes
$timeremainingminutesavailable = $timeremainingminutes * .60
$timeremainingminutesavailable = [Double]$timeremainingminutesavailable
Write-Host "Minutes Available"
$timeremainingminutesavailable
$timeremaininghoursavailable = [Math]::truncate($timeremaining)
$timeremaininghoursavailable = [Double]$timeremaininghoursavailable
Write-Host "Hours Available"
$timeremaininghoursavailable
$totalhours = Read-Host "Totalhours on timesheet now"
$totalhours = [Double]$totalhours
$totalhoursnow = $totalhours + $t
$totalhoursnow = [Double]$totalhoursnow
Write-Host "Total Hours now"
$totalhoursnow
$hoursequal40 = 40 - $totalhoursnow 
$hoursequal40 = [Double]$hoursequal40
Write-Host "What is left to equal 40 hours"
$hoursequal40
$timefixminutes = $hoursequal40 - [Math]::truncate($hoursequal40)
$timefixminutes = [Double]$timefixminutes
Write-Host "What is left to equal 40 in minutes part"
$timefixminutes
$timefixremainingminutesavailable = $timefixminutes * .60
$timefixremainingminutesavailable = [Double]$timefixremainingminutesavailable
Write-Host "Minutes Available in time"
$timefixremainingminutesavailable
$timefixremaininghoursavailable = [Math]::truncate($hoursequal40)
$timefixremaininghoursavailable = [Double]$timefixremaininghoursavailable
Write-Host "What is left to equal 40 Hours part (Available add or subtract)"
$timefixremaininghoursavailable
$timeadj = Read-Host "Timeadj"
$timeadjsplit = ($timeadj).split(":")
$timeadjsplit[0] = [Double]$timeadjsplit[0]
$timeadjsplit[1] = [Double]$timeadjsplit[1]
$decimin = $timeadj[1] / 100
$decimin = [Double]$decimin
$adjhour = $clockoutsplit[0] + $timeadjsplit[0]
$adjhour = [Double]$adjhour
$adjhour
$adjmin = $decimin + $decimal3
$adjmin = [Double]$adjmin
$adjmin
