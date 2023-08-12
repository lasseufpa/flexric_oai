# FlexRIC and OpenAirInterface

Necessary: This setup uses the USRP B210 connected via USB 3.0. To execute the code, it needs to remain connected.

## Environment
  - Clone this repository: `git clone https://github.com/lasseufpa/flexric_oai.git`

### Building the image of FlexRIC and OAI (OpenAirInterface)

Enter in this folder: ` cd flexric_oai`
- First, create the image in your computer (This step takes a little while):
  ```
  cd BaseStation_Docker
  docker build -t flexric -t flexric
  docker build -t oai -t oai
  ```

with this commands, you will create the images that it'll use in docker compose
  
- Then, execute the docker compose:
  ```
  docker compose up
  ```
  or 
  ```
  docker compose up -d
  ```
  To hide the log.

- To view FlexRIC's log when it is hidden, enter this command.
  ```
  docker logs Flexric
  ```
