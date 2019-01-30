# loginDemo docker

This repo is to setup the login demo using docker, it creates multiple containers via docker-compose to act as one application.

To use it `git clone` this repo and `cd` to the root of the repo, then run `docker-compose build --force-rm --no-cache` after building run `docker-compose up -d` to start the containers. After the containers are up you should be able to use a web browser and navigate to the host via `http://domain-or-ip/`

To stop the containers run `docker-compose down`

look at the /docker-compose.yml, /server/Dockerfile and /client/Dockerfile on how it's all brought together.

## Info<br>
Client is the only container that has a port(80) that is accessible outside the bridged network for the host.<br>
Check out [Docker](https://www.docker.com/) if you don't know what this is all about.<br>

[login client](https://github.com/Darkrm/logindemo.client)<br>
[login server](https://github.com/Darkrm/logindemo.server)<br>

A seed account is added to the database at runtime to allow you to login.

login : test@test.com<br>
password : test

## License

The contents of this repository is not licensed out. You may not run, copy, modify or use anypart of it without the express written consent of the copyright holder.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
