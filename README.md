import random

# Daftar kata kunci dan respons
keywords = {
  "halo": ["Halo juga!", "Hai!"],
  "apa kabar?": ["Baik-baik saja, terima kasih.", "Sedang sibuk. Kamu sendiri?"],
  "siapa namamu": ["Saya Chatbot.", "Saya tidak punya nama."],
  "selamat tinggal": ["Sampai jumpa!", "Hingga nanti!"],
  "anjing lu": ["anjing juga"]
}

# Fungsi untuk memberikan respons berdasarkan input
def give_response(user_input):
  # Mengubah input menjadi huruf kecil untuk memudahkan pencarian
  user_input = user_input.lower()

  # Pencarian kata kunci pada input
  for keyword in keywords:
    if keyword in user_input:
      # Mengembalikan respons acak dari daftar respons
      return random.choice(keywords[keyword])

  # Jika tidak ada kata kunci yang cocok, kembalikan pesan default
  return "Maaf, saya tidak mengerti apa yang kamu maksud."

# Loop utama untuk menerima input pengguna dan memberikan respons
while True:
  # Menerima input dari pengguna
  user_input = input("Anda: ")

  # Memberikan respons menggunakan fungsi give_response
  bot_response = give_response(user_input)

  # Mencetak respons dari chatbot
  print("Chatbot:", bot_response)
