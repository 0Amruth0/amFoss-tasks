mkdir Coordinates-Location
cd Coordinates-Location/
mkdir North
cd North/
touch NDegree.txt
a=$((5*5-4*2*2))
echo $a>NDegree.txt
b=$a°
echo $b>NDegree.txt
touch NMinutes.txt
a=5
b=$a"'"
echo $b>NMinutes.txt
touch NSeconds.txt
a=38
x=0.1
b=`echo $a+$x | bc`
c=$b'"'
echo $c>NSeconds.txt
cat NDegree.txt NMinutes.txt NSeconds.txt | tr -d '\n' >>NorthCoordinate.txt
cp -r NorthCoordinate.txt /home/amruth/Desktop/~repositories/amFoss-tasks/task-02/Coordinates-Location/
cd ~
cd Desktop/~repositories/amFoss-tasks/task-02/Coordinates-Location/
mv NorthCoordinate.txt North.txt
cd North/
rm NorthCoordinate.txt 
cd ~
cd Desktop/~repositories/amFoss-tasks/task-02/Coordinates-Location/
mkdir East
cd East/
touch EDegree.txt
a=76
b=$a°
echo $b>EDegree.txt
touch EMinutes.txt
a=29
b=$a"'"
echo $b>EMinutes.txt
touch ESeconds.txt
a=30
y=0.8
b=`echo $a+$y | bc`
c=$b'"'
echo $c>ESeconds.txt
cat EDegree.txt EMinutes.txt ESeconds.txt | tr -d '\n' >>EastCoordinates.txt
cp -r EastCoordinates.txt /home/amruth/Desktop/~repositories/amFoss-tasks/task-02/Coordinates-Location/
cd ~
cd Desktop/~repositories/amFoss-tasks/task-02/Coordinates-Location/
mv EastCoordinates.txt East.txt
cd East/
rm EastCoordinates.txt 
cd ~
cd Desktop/~repositories/amFoss-tasks/task-02/Coordinates-Location/
cat North.txt East.txt | tr -d '\n' >> Location-Coordinates.txtS
git add task-02
git commit -m "updates"
git push originmaster
