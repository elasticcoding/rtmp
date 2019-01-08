# rtmp
This is a container for Nginx-Rtmp
The RTMP module from 
https://github.com/arut/nginx-rtmp-module

How to Do this
1) clone the repo
2) install docker
3) build the docker image from docker file ( docker build -t nginx-rtmp .)
4) run the docker (docker run -d -p 80:80 -p 1935:1935  --name nginx-rtmp nginx-rtmp)


for FFmpeg

run all above command except (4)

4) docker run -d -v /home/xion/Documents/streaming/live:/usr/local/nginx/conf/live -v /home/xion/Documents/streaming/apps:/usr/local/nginx/conf/apps -p 80:80 -p 1935:1935 --name nginx-rtmp nginx-rtmp


#HOW TO STREAM A VIDEO

1) push rtmp video stream to the server rtmp://IP:1935/live/(any-stream-key)
2) pull the same video by vlc or any player rtmp://IP:1935/live/(same-key-that-uses-the-push)
3) To check the status of it http://IP:80/status

Copyright 2019 Shouvik Ghosh

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
