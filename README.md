1. Prepare gif with https://ezgif.com (crop -> resize -> split - skip frames -> save). (Keep in mind that TTGO can store ~15 frames)
2. Register and create new token on OpenWeatherMap API. (They send it right after registration by Email, API key is active after 30min);
3. Update code with city, conuntry, api key, time-zone converter, wifi credentials;
4. Prepare gif with gif-converter:
```
pyenv install 3.9.0
pyenv local 3.9.0
pip install Pillow
brew install ghostscript
brew install imagemagick
```
5. Fix path to imagemack in eTFT-gif-converter.py
```
cmd = ['/usr/local/bin/convert', '-coalesce', self.gif, 'frame_%d.jpg']
```
6. Generate animation header file:
```
cd gif-converter/
./eTFT-gif-converter.py -i ~/Downloads/222.gif -o ../ani.h
```
7. Compile with Arduino IDE
8. Debug Serial on 115200
10. Have fun!
