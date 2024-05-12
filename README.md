import random


questions = [
    {
        "question": "Ai là người đầu tiên bước lên mặt trăng?",
        "options": ["A. Neil Armstrong", "B. Buzz Aldrin", "C. Yuri Gagarin", "D. John Glenn"],
        "answer": "A"
    },
    {
        "question": "Thủ đô của nước nào là Paris?",
        "options": ["A. Ý", "B. Đức", "C. Pháp", "D. Tây Ban Nha"],
        "answer": "C"
    },
    {
        "question": "Số Pi bằng bao nhiêu?",
        "options": ["A. 3,14", "B. 3.1415926535897932384626433832795028841971693993751058209749445923078164062862089986280348253421170679", "C. 3","D. π"],
        "answer": "D"
    },
    {
        "question": "Bao lâu nữa thì bán được 1 tỷ gói mè?"
        "options":["A. làm thế quái nào mà nhập được 1 tỷ gói mè","B. 33 năm","C. 2000 năm","D. 1 gói mè giá 10 000 đ thì 1 tỷ gói mè bằng 10 000 tỷ đồng à"]
        "answer":"D"
    },
    {
        "question":"Chữ đầu tiên tromg bảng chữ cái latin là gì?"
        "options":["A. D","B. Y","C. A","D. B"]
        "answer":"C"
    },
    {
        "question":""
    }

]           


def check_answer(question, answer):
    return question["answer"] == answer


def play_game():
    score = 0
    random.shuffle(questions)
    for i, question in enumerate(questions):
        print(f"Câu hỏi {i+1}: {question['question']}")
        for option in question["options"]:
            print(option)
        user_answer = input("Chọn đáp án (A/B/C/D): ").upper()
        if check_answer(question, user_answer):
            print("Chính xác! Bạn đã thắng 1000 điểm.")
            score += 1000
        else:
            print("Sai rồi! Bạn không thể tiếp tục chơi.")
            break
    print(f"Điểm của bạn: {score}")


play_game()
