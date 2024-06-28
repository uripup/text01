# text01

yyyy-mm 처리

import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;

public static Date inputDate(String format, Object... args) {
    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM");
    while (true) {
        try {
            String input = input(format, args);
            // 입력받은 yyyy-MM에 "-01"을 추가하여 yyyy-MM-dd 형식으로 만듭니다.
            Date date = sdf.parse(input + "-01");
            return date;
        } catch (ParseException e) {
            System.out.println("날짜 형식이 잘못되었습니다. yyyy-MM 형식으로 입력해주세요.");
        }
    }
}
