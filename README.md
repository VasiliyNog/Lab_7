# Variant№ 8
Public class Svedenia {
    private static final Object PNOTE = ;

    public static void main(String[] args) {
        using namespace Object std;
        std;

        struct {
            string fam, name;
            int birdthdate[ 3];
        
    } typedef NOTE, *PNOTE;

        int main () {
            vector<PNOTE> notebook;

            while (true) {
                PNOTE note = new NOTE;
                cout << "Vvedite familiy: ";
                cin >> note -> fam;
                cout << "Vvedite imya: ";
                cin >> note -> name;
                cout << "Birdth (dd mm yyyy): ";
                cin >> note -> birdthdate[0];
                cin >> note -> birdthdate[1];
                cin >> note -> birdthdate[2];
                notebook.push_back(note);
                cout << "Vvesti eshe (y/n)? ";
                char ch;
                cin >> ch;
                if (ch == 'n' || ch == 'N') break;
            }

            int occur = 0, month;
            cout << "Enter month: ";
            cin >> month;

            for (auto v : notebook)  // <---------------------------------------
            {
                if (v -> birdthdate[1] == month) {
                    cout << v -> fam << " " << v -> name << " " <<
                            v -> birdthdate[0] << "/" << v -> birdthdate[1] <<
                                    "/" << v -> birdthdate[2] << endl;
                    ++occur;
                }
            }
            if (!occur)
                cout << "Takih net!" << endl;

            for (auto v : notebook)
                delete v;

            return 0;
        }
    }
}
