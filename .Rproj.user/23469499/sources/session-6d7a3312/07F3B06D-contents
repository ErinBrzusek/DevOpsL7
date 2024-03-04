from vetiver import VetiverModel
from dotenv import load_dotenv, find_dotenv
import vetiver
import pins

load_dotenv(find_dotenv())

b = pins.board_folder('data/model', allow_pickle_read=True)
v = VetiverModel.from_pin(b, 'penguin_model', version = '20240302T142248Z-a6f9b')

vetiver_api = vetiver.VetiverAPI(v)
api = vetiver_api.app

# Similar to app.run call; runs API with provided host and port
if __name__ == "__main__":
  import uvicorn
  uvicorn.run(api, host = "127.0.0.1", port = 8080)

