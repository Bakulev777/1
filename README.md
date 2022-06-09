# 
import telebot
import time
import random
from telebot import types

bot=telebot.TeleBot("Токен")

@bot.message_handler(commands=['start'])
def start(message):
    mess=f'Привет {message.from_user.first_name} {message.from_user.last_name}'
    bot.send_message(message.chat.id, mess)
@bot.message_handler(content_types=['text'])
def get_user_text(message):
    if message.text == "Привет":
        bot.send_message(message.chat.id, f'Привет {message.from_user.first_name} {message.from_user.last_name} , если хочешь увидеть как я выгляжу то напиши "Покажи себя , сразу скажу, что я лучше понимаю, когда пишут начиная с Заглавной буквы и ставят перед знаками преминания пробел, иначе мне тяжело еще читать"')
    elif message.text =='id':
        bot.send_message(message.chat.id, f'Твой ID: {message.from_user.id}')
    elif message.text == 'Как тебя зовут ?':
        bot.send_message(message.chat.id, "меня зовут Эдгар Бакулев а тебя ? ")
    elif message.text == 'Как дела ?':
        bot.send_message(message.chat.id, "да, пойдет, Мурка ходит беременная , муричит, как сам)? ")
    elif message.text == 'Как дела?':
        bot.send_message(message.chat.id, "Да без рэкета получше стало а ты ?  ")
    elif message.text == 'Что делаешь ?':
        bot.send_message(message.chat.id, "Валяюсь , колбасу точу, муська прикимарила на лежанке тут  ")
    elif message.text == 'Что делаешь?':
        bot.send_message(message.chat.id, "Срать собирался только... а ты ??? ")
    elif message.text == 'Хорошо':
        bot.send_message(message.chat.id, "ну самое главное что все хорошо ")
    elif message.text == 'Как зовут маму ?':
        bot.send_message(message.chat.id, "Алина Бакулева, обожаю ее ")
    elif message.text == 'Как маму зовут ?':
        bot.send_message(message.chat.id, "Алина Бакулева, обожаю ее ")
    elif message.text == 'Какое имя у  мамы ?':
        bot.send_message(message.chat.id, "Алина Бакулева, обожаю ее ")

    elif message.text == 'Как папу зовут ?':
        bot.send_message(message.chat.id, "Илья Бакулев я его люблю ")

    elif message.text == 'Илья':
        bot.send_message(message.chat.id, "Отец мой)))")

    elif message.text == 'Алина':
        bot.send_message(message.chat.id, "Мамку никому не отдам ")

    elif message.text == 'Ты хороший)':
        bot.send_message(message.chat.id, "Спасибо)) ")

    elif message.text == 'Эдгар':
        bot.send_message(message.chat.id, "да, да я тут что хотите? ")

    elif message.text == 'Покажи себя':
        photo=open('111.png', 'rb')
        bot.send_document (message.chat.id, photo)

    elif message.text == 'Ты красивый':
        bot.send_message(message.chat.id, "Да я знаю спасибо , ты тоже ничего ")

    elif message.text == 'Как погода ?':
        bot.send_message(message.chat.id, "Да отличная , пошли гулять ?")

    elif message.text == 'Тебе сколько лет ?':
        bot.send_message(message.chat.id, "Лет 20-25 по человеческому !")

    elif message.text == 'У тебя есть дети ?':
        bot.send_message(message.chat.id, "Да муська беременная , скоро будут, на продажу пойдут, стану богатым)))")

    elif message.text == 'привет':
        bot.send_message(message.chat.id, "Привет, сразу скажу, что я лучше понимаю, когда пишут начиная с Заглавной буквы и ставят перед знаками преминания пробел, иначе мне тяжело еще читать")


    elif message.text == 'Ты старый ?' :
        bot.send_message(message.chat.id, "Еше тебе форму дам ")

    elif message.text == 'Что будешь делать ?':
        bot.send_message(message.chat.id, "С муськой планируем фильмы смотреть вечерком")

    elif message.text == 'Какая сегодня погода ?':
        bot.send_message(message.chat.id, "Жара, захотелось на озеро у меня есть маска для ныряния ")

    elif message.text == 'Пока':
        bot.send_message(message.chat.id, "Ну давай пока")

    elif message.text == 'Ты где?':
        bot.send_message(message.chat.id, "Дома тут травку курю а ты ")

    elif message.text == 'А папу ?':
        bot.send_message(message.chat.id, "Илюха")

    elif message.text == 'Как сегодня погода ?':
        bot.set_chat_description(message.chat.id, "Я устал ")


    elif message.text == 'Измени название чата':
        bot.set_chat_title(message.chat.id, f'{message.from_user.first_name}')

    elif message.text == 'Игра':
        bot.set_chat_description(message.chat.id, "Я устал ")

    elif message.text == 'Кто такой Русик ?':
        bot.send_message(message.chat.id, "Да, есть один жирдяй, брат папы ")

    elif message.text == 'Что сегодня будешь делать ?':
        bot.send_message(message.chat.id, "Да дома поваляюсь, колбасу есть а ты ? ")

    elif message.text == 'Ничего':
        bot.send_message(message.chat.id, "Всмысле ничего ? ")

    elif message.text == 'Нет':
        bot.send_message(message.chat.id, "Всмысле нет ? ")

    elif message.text == 'Да':
        bot.send_message(message.chat.id, "да - yes ")

    elif message.text == 'Я гулять':
        bot.send_message(message.chat.id, "ну давай , погуляешь, набери  ")

    elif message.text == 'Я домой':
        bot.send_message(message.chat.id, "ну давай , погуляешь, набери  ")

    elif message.text == 'Ты где?':
        bot.send_message(message.chat.id, " на лотке сижу сру ")

    elif message.text == 'Ты где ?':
        bot.send_message(message.chat.id, " на лотке сижу сру ")


    elif message.text == 'ты где?':
        bot.send_message(message.chat.id, " на лотке сижу сру ")

    elif message.text == 'скинь фото':
        bot.send_message(message.chat.id, " мою на лотке фотку?  ")

    elif message.text == 'Скинь фотку':
        bot.send_message(message.chat.id, " мою на лотке фотку?  ")

    elif message.text == 'Скинь фотку':
        bot.send_message(message.chat.id, " мою на лотке фотку?  ")

    elif message.text == 'Я иду':
        bot.send_message(message.chat.id, " куда идешь ?  ")

    elif message.text == 'Да уж':
        bot.send_message(message.chat.id, " хуяуж  ")

    elif message.text == 'Ты где живёшь ?':
        bot.send_message(message.chat.id, " В питере живу с мамкой а ты сейчас где?  ")

    elif message.text == 'Я дома':
        bot.send_message(message.chat.id, " Фух, я спокоен, я тоже дома ")

    elif message.text == 'Я на работу':
        bot.send_message(message.chat.id, " а ты где работаешь? ")

    elif message.text == 'Ты когда домой?':
        bot.send_message(message.chat.id, " скоро прийдет уже)  ")

    elif message.text == 'Завтра':
        bot.send_message(message.chat.id, " Хуявтра ")

    elif message.text == 'Сегодня':
        bot.send_message(message.chat.id, " Во сколько сегодня?  ")


    elif message.text == 'пошли':
        bot.send_message(message.chat.id, " куда? ")

    elif message.text == 'ты где ?':
        bot.send_message(message.chat.id, " на кровати с муськой ")

    elif message.text == 'Давай':
        bot.send_message(message.chat.id, " Она тебе не даст )))  ")
    elif message.text == 'завтра':
        bot.send_message(message.chat.id, " Хуявтра ")

    elif message.text == 'Бля':
        bot.send_message(message.chat.id, " не могу слушать маты(((( ")

    elif message.text == 'Не спишь?':
        bot.send_message(message.chat.id, " я никогда не сплю)) брожу по комнате ")

    elif message.text == 'Сижу':
        bot.send_message(message.chat.id, " Иди ложись поспи ")

    elif message.text == 'нет':
        bot.send_message(message.chat.id, " Пидора ответ хи хи хи  ")

    elif message.text == 'завтра':
        bot.send_message(message.chat.id, " Хуявтра ")

    elif message.text == 'Ты дома ?':
        bot.send_message(message.chat.id, " на лотке , говорю же ")

    elif message.text == 'Соскучился?':
        bot.send_message(message.chat.id, " немного скучаю да уже ")


    elif message.text == 'Спать ?':
        bot.send_message(message.chat.id, " Never sleep ")

    elif message.text == 'Я кушать':
        bot.send_message(message.chat.id, " приятного аппетита ")

    elif message.text == 'Спасибо':
        bot.send_message(message.chat.id, " Не за что  ")

    elif message.text == 'Извини':
        bot.send_message(message.chat.id, " Нет тебе прощения стерва  ")

    elif message.text == 'Хорошо':
        bot.send_message(message.chat.id, " ХОРОШО Это когда есть корм в кормушке ")

    elif message.text == 'Отвали':
        bot.send_message(message.chat.id, " Сам отвали  ")

    elif message.text == 'Гулять?':
        bot.send_message(message.chat.id, " Я тоже гулять хочу(( возьмите с собой ")

    elif message.text == 'Хорошо':
        bot.send_message(message.chat.id, " хорошо )) ")

    elif message.text == '))':
        bot.send_message(message.chat.id, " Че лыбимся)? ")

    elif message.text == 'Вечером?':
        bot.send_message(message.chat.id, " с папкой любим вечерами гулять  ")

    elif message.text == 'Мама':
        bot.send_message(message.chat.id, " мою мамку Алинка зовут)))  ")

    elif message.text == 'Папа':
        bot.send_message(message.chat.id, " Папу Илюха зовут, он умный у меня  ")

    elif message.text == 'Красивый':
        bot.send_message(message.chat.id, " Спасибо ты тоже ничего ")

    elif message.text == 'спасибо':
        bot.send_message(message.chat.id, " Пожалуйста))  ")


    elif message.text == 'Он':
        bot.send_message(message.chat.id, " Кто он)?  ")

    elif message.text == 'Она':
        bot.send_message(message.chat.id, " Кто она )? ")

    elif message.text == 'Кот':
        bot.send_message(message.chat.id, " Я кот из магазина Сезон, мой отец Илья а мама Алина , она меня забрала от варваров магазинных ")

    elif message.text == 'Что?':
        bot.send_message(message.chat.id, " Ты о чем )? ")

    elif message.text == 'Сезон':
        bot.send_message(message.chat.id, " Меня забрали из этого магазина да да   ")

    elif message.text == 'Отец':
        bot.send_message(message.chat.id, " Илья его звать) Бакулев ")

    elif message.text == 'Мамка':
        bot.send_message(message.chat.id, " Маму зовут Алина же Бакулева  ")

    elif message.text == 'Рекет':
        bot.send_message(message.chat.id, " Я уже больше не занимаюсь этим")

    elif message.text == 'Гавно':
        bot.send_message(message.chat.id, " Гавно это мое любимое слово ")

    elif message.text == 'Срать':
        bot.send_message(message.chat.id, " То что я люблю делать по вечерам на лотке) пошли со мной? ")
    
    elif message.text == 'Я':
        bot.send_message(message.chat.id, " что ты ?")

    elif message.text == 'Дома':
        bot.send_message(message.chat.id, " Твой дом это тоже лоток ?")

    elif message.text == 'Тебя как зовут?':
        bot.send_message(message.chat.id, " Эдгар Бакулев , рекетир Санкт Петербурга?")

    elif message.text == 'Ем':
        bot.send_message(message.chat.id, "и так есть лишний вес ")

    elif message.text == 'Лежу':
        bot.send_message(message.chat.id, "Вставай заниматься спортом ")

    elif message.text == 'Жру':
        bot.send_message(message.chat.id, "куда еще? весы сломались старые  ")

    elif message.text == 'Кушаю':
        bot.send_message(message.chat.id, "куда еще? весы сломались старые ")

    elif message.text == 'Лоток':
        bot.send_message(message.chat.id, "мое любимое место это лоток ")

    elif message.text == 'Туалет':
        bot.send_message(message.chat.id, "Посрать я люблю)) ")

    elif message.text == 'Корм':
        bot.send_message(message.chat.id, "Смотря какой корм, вискас лучше не предлагать ")

    elif message.text == 'Пошли вместе':
        bot.send_message(message.chat.id, "куда пойдем? ")

    elif message.text == 'Гулять?':
        bot.send_message(message.chat.id, "А кто пойдет ?")

    elif message.text == 'Сука':
        bot.send_message(message.chat.id, "Сука это мат или нет?  ")

    elif message.text == 'Угар))':
        bot.send_message(message.chat.id, "ЧЕ УГОРАЕШЬ? ")

    elif message.text == 'Пиздец':
        bot.send_message(message.chat.id, "Никакой не пиздец, все заебись)))) ")

    elif message.text == 'Гороскоп':
        bot.send_message(message.chat.id, "Привет, сейчас я расскажу тебе гороскоп на сегодня.")
        keyboard = types.InlineKeyboardMarkup()
        # По очереди готовим текст и обработчик для каждого знака зодиака
        key_oven = types.InlineKeyboardButton(text='Овен', callback_data='zodiac')
        # И добавляем кнопку на экран
        keyboard.add(key_oven)
        key_telec = types.InlineKeyboardButton(text='Телец', callback_data='zodiac')
        keyboard.add(key_telec)
        key_bliznecy = types.InlineKeyboardButton(text='Близнецы', callback_data='zodiac')
        keyboard.add(key_bliznecy)
        key_rak = types.InlineKeyboardButton(text='Рак', callback_data='zodiac')
        keyboard.add(key_rak)
        key_lev = types.InlineKeyboardButton(text='Лев', callback_data='zodiac')
        keyboard.add(key_lev)
        key_deva = types.InlineKeyboardButton(text='Дева', callback_data='zodiac')
        keyboard.add(key_deva)
        key_vesy = types.InlineKeyboardButton(text='Весы', callback_data='zodiac')
        keyboard.add(key_vesy)
        key_scorpion = types.InlineKeyboardButton(text='Скорпион', callback_data='zodiac')
        keyboard.add(key_scorpion)
        key_strelec = types.InlineKeyboardButton(text='Стрелец', callback_data='zodiac')
        keyboard.add(key_strelec)
        key_kozerog = types.InlineKeyboardButton(text='Козерог', callback_data='zodiac')
        keyboard.add(key_kozerog)
        key_vodoley = types.InlineKeyboardButton(text='Водолей', callback_data='zodiac')
        keyboard.add(key_vodoley)
        key_ryby = types.InlineKeyboardButton(text='Рыбы', callback_data='zodiac')
        keyboard.add(key_ryby)
        # Показываем все кнопки сразу и пишем сообщение о выборе

@bot.callback_query_handler(func=lambda call: True)
def callback_worker(call):
    # Если нажали на одну из 12 кнопок — выводим гороскоп
    if call.data == "zodiac":
        # Формируем гороскоп
        msg = random.choice(first) + ' ' + random.choice(second) + ' ' + random.choice(second_add) + ' ' + random.choice(third)
        # Отправляем текст в Телеграм
        bot.send_message(call.message.chat.id, msg)

















@bot.message_handler(content_types=['photo'])
def get_user_photo(message):
    bot.send_message(message.chat.id, "Вау, ОГОНЬ фотка!!! ")

@bot.message_handler(content_types=["sticker"])
def get_user_sticker(message):
    bot.send_message(message.chat.id, "Стикеры мамка сделала огонь, каждый раз угораю)) ")

@bot.message_handler(commands=['website'])
def website(message):
    markup=types.InlineKeyboardMarkup()
    markup.add(types.InlineKeyboardButton('Посетить гавно', url='yandex.ru'))
    bot.send_message(message.chat.id, "Нажми сюда", reply_markup=markup)

@bot.message_handler(commands=['help'])
def website(message):
    markup=types.ReplyKeyboardMarkup
    website= types.KeyboardButton("Веб")
    start=tu=types.KeyboardButton("Start")

    markup.add(website, start )
    bot.send_message(message.chat.id, "Нажми сюда", reply_markup=markup)


first = ["Сегодня — идеальный день для новых начинаний.","Оптимальный день для того, чтобы решиться на смелый поступок!","Будьте осторожны, сегодня звёзды могут повлиять на ваше финансовое состояние.","Лучшее время для того, чтобы начать новые отношения или разобраться со старыми.","Плодотворный день для того, чтобы разобраться с накопившимися делами."]
second = ["Но помните, что даже в этом случае нужно не забывать про","Если поедете за город, заранее подумайте про","Те, кто сегодня нацелен выполнить множество дел, должны помнить про","Если у вас упадок сил, обратите внимание на","Помните, что мысли материальны, а значит вам в течение дня нужно постоянно думать про"]
second_add = ["отношения с друзьями и близкими.","работу и деловые вопросы, которые могут так некстати помешать планам.","себя и своё здоровье, иначе к вечеру возможен полный раздрай.","бытовые вопросы — особенно те, которые вы не доделали вчера.","отдых, чтобы не превратить себя в загнанную лошадь в конце месяца."]
third = ["Злые языки могут говорить вам обратное, но сегодня их слушать не нужно.","Знайте, что успех благоволит только настойчивым, поэтому посвятите этот день воспитанию духа.","Даже если вы не сможете уменьшить влияние ретроградного Меркурия, то хотя бы доведите дела до конца.","Не нужно бояться одиноких встреч — сегодня то самое время, когда они значат многое.","Если встретите незнакомца на пути — проявите участие, и тогда эта встреча посулит вам приятные хлопоты."]

@bot.message_handler(content_types=['text'])
def get_text_messages(message):
    if message.text == "Гороскоп":
        bot.send_message(message.from_user.id, "Привет, сейчас я расскажу тебе гороскоп на сегодня.")
        # Готовим кнопки
        keyboard = types.InlineKeyboardMarkup()
        # По очереди готовим текст и обработчик для каждого знака зодиака
        key_oven = types.InlineKeyboardButton(text='Овен', callback_data='zodiac')
        # И добавляем кнопку на экран
        keyboard.add(key_oven)
        key_telec = types.InlineKeyboardButton(text='Телец', callback_data='zodiac')
        keyboard.add(key_telec)
        key_bliznecy = types.InlineKeyboardButton(text='Близнецы', callback_data='zodiac')
        keyboard.add(key_bliznecy)
        key_rak = types.InlineKeyboardButton(text='Рак', callback_data='zodiac')
        keyboard.add(key_rak)
        key_lev = types.InlineKeyboardButton(text='Лев', callback_data='zodiac')
        keyboard.add(key_lev)
        key_deva = types.InlineKeyboardButton(text='Дева', callback_data='zodiac')
        keyboard.add(key_deva)
        key_vesy = types.InlineKeyboardButton(text='Весы', callback_data='zodiac')
        keyboard.add(key_vesy)
        key_scorpion = types.InlineKeyboardButton(text='Скорпион', callback_data='zodiac')
        keyboard.add(key_scorpion)
        key_strelec = types.InlineKeyboardButton(text='Стрелец', callback_data='zodiac')
        keyboard.add(key_strelec)
        key_kozerog = types.InlineKeyboardButton(text='Козерог', callback_data='zodiac')
        keyboard.add(key_kozerog)
        key_vodoley = types.InlineKeyboardButton(text='Водолей', callback_data='zodiac')
        keyboard.add(key_vodoley)
        key_ryby = types.InlineKeyboardButton(text='Рыбы', callback_data='zodiac')
        keyboard.add(key_ryby)
        # Показываем все кнопки сразу и пишем сообщение о выборе







bot.polling(none_stop=True)
