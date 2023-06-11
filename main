import datetime
import os

import requests

if __name__ == '__main__':
    base_path = '/home/mohsen/PycharmProjects/personal/sparktestyard/scraping/tse/'
    response = requests.get('https://tse.ir/json/MarketWatch/MarketWatch_1.xls', verify=False)
    if response.status_code == 200:
        now = datetime.datetime.now().strftime('%Y-%m-%d_%H-%M-%S.%f')
        file_path = os.path.join(base_path, f'Market_{now}.xls')
        with open(file_path, 'wb') as f:
            f.write(response.content)
    else:
        print('Error occurred during file download')
