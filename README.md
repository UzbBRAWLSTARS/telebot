# telebotimport random

from aiogram import Bot, Dispatcher, executor, types
API_TOKEN ='6319197101:AAE7bISYOkF1Nf69aW9B3MaWg3q5PgbiUV4'

logging.basicConfig(level=logging.INFO)

bot = Bot(token=API_TOKEN)
dp = Dispatcher(bot)
javob=int(input())

@dp.message_handler(commands=['start', 'help'])
async def send_welcome(message: types.Message):
    await message.reply("Salom keling o'yin o'ynaymiz🧩")

types.ReplyKeyboardMarkup(row_width=2,resize_keyboard=True)
    keys.add(
        types.KeyboardButton(text="✔️Son o'yini🔥"),
        types.KeyboardButton(text="stop")
        await message.reply("Salom",reply_markup=keys)
    
    
@dp.message_handler(text="✔️Son o'yini🔥")
async def bozi(message:types.Message):
    await message.answer("Men 1 dan 100 gacha bir son o'yaldim qani siz topa olasizmi")
    
    def t_son():
        son = random.randint(1, 100)
        attempts = 0
        while True:
            javob = int(input("Raqamni kiriting :"))
            attempts += 1
            if javob>son:
                await message.answer("Men o'ylagan son bundan kichikroq")
            elif javob<son:
                await message.answer("Men o'ylagan son bundan kattaroq")
            else:
                await message.answer("🎉Siz topdingiz! men ",son," sonini o'ylagan edim")
                break
    t_son()
    
    

if name=='main':
    executor.start_polling(dp,skip_updates=True 
