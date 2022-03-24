import time
import asyncio
import sys
import re
import threading
from random import randint
from time import sleep
from telethon import TelegramClient, events, utils
from telethon.tl.functions.messages import GetBotCallbackAnswerRequest

api_id = 2192634
api_hash = '64851927b0dad3f4460a24e3da7b0822'
sesi_fil = 'TeaOS'
chat = 'kampungmaifambot'

def Tea():
    loop = asyncio.new_event_loop()
    asyncio.set_event_loop(loop)
    with TelegramClient(sesi_fil, api_id, api_hash, loop=loop) as client:
        client.loop.run_until_complete(client.send_message(chat,'/casino_FiftyFifty_'+str(randint(1,2))+'_1000000000000'))
        @client.on(events.NewMessage(from_users=chat))
        async def handler(event):
            global wait
                    
            if 'Berhasil bertaruh' in event.raw_text:
                time.sleep(61)
                await event.respond('/casino_hasil')
                return
            if 'yang menang adalah' in event.raw_text:
                time.sleep(2)
                await event.respond('/casino_FiftyFifty_'+str(randint(1,2))+'_1000000000000')
                return
            if 'Target EXP tercapai,' in event.raw_text:
                time.sleep(1)
                await event.respond('/casino_FiftyFifty_'+str(randint(1,2))+'_1000000000000')
                return
            
        client.run_until_disconnected()
        print(time.asctime(), '-', 'Stop')
threading.TIMEOUT_MAX
threading.Thread(target=Tea).start()
print(time.asctime(), '-', 'Start')
