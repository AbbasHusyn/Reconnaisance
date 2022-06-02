echo "_________________________________________________________________________________"
echo "Purpose of this script is to gather information related to any Domain"
echo "This script is design by Syed Abbas Hussain - Masters in Information Security"
echo "Purpose of the script is purely based on self learning"
echo "No attack or ransome has been lodge during this activity"
echo "Learn and Enjoy"
echo "_________________________________________________________________________________"
echo
echo
echo "This script will perform following operations"
echo "1- Whois"
echo "2- Sublister"
echo "3- The Harvestor"
echo "4- NSlookup"
echo "5- DNSenum"
echo
echo "Type any URL"
read URL
echo
for i in $(seq 1 5); do
echo "Which operation you want to perform"
read ops
echo
case $ops in
1) echo "You have selected Whois";;
2) echo "You have selected Sublister";;
3) echo "You have selected The Harvestor";;
4) echo "You have selected NSLookup";;
5) echo "You have selected DNS Enumerator"
esac
echo
if [ $ops -eq 1 ] ; then
echo "Resuls of Whois commands is pasted below"
echo
whois $URL
echo
echo
elif [ $ops -eq 2 ] ; then
echo "Results of Sublisted command is pasted below"
echo
sublist3r -d $URL
echo
echo
elif [ $ops -eq 3 ] ; then
echo "Results of The Harvestor command is pasted below"
echo
theHarvester -d $URL -l 500 -b google
echo
echo
elif [ $ops -eq 4 ] ; then
echo "Results of NSLookup command is pasted below"
echo
nslookup $URL
echo
echo
elif [ $ops -eq 5 ] ; then
echo "Results of DNSenum command is pasted below"
echo
dnsenum $URL
echo
echo
fi
done
