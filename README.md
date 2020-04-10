# newprogram
namespace Online_Shopping
{
    public partial class Gamestore : Form
    {
        public Gamestore(string input)
        {
            InitializeComponent();

            if (input == "xbox")
            {
                lstGames.Items.Add("Forza Horizon 7");
                lstGames.Items.Add("PLAYERUNKNOWNS BATTLEGROUNDS");
                lstGames.Items.Add("Anthem");
                lstGames.Items.Add("Crash Bandicoot: N'Sane Trilogy");
                lstGames.Items.Add("Spyro Reignited Trilogy");
                lstGames.Items.Add("Star Wars Jedi: Fallen order");
                lstGames.Items.Add("Battlefield V");
                lstGames.Items.Add("Star Wars: Battlefront 2");
                lstGames.Items.Add("Division 2");
                lstGames.Items.Add("Shadow of the Tomb Raider");
            }
            else
            {
                lstGames.Items.Add("The Last Of Us Remastered");
                lstGames.Items.Add("Uncharted 4: A Thief's End");
                lstGames.Items.Add("God Of War");
                lstGames.Items.Add("Ratchet & Clank");
                lstGames.Items.Add("Little BIG Planet 3");
                lstGames.Items.Add("Days Gone");
                lstGames.Items.Add("Far Cry 5");
                lstGames.Items.Add("Spider-Man");
                lstGames.Items.Add("Call of Duty: Modern Warfare");
                lstGames.Items.Add("Dark Souls 3");
            }
        }

        public void lstGames_SelectedIndexChanged(object sender, EventArgs e)
        {
            MainMenu mainmenu = new MainMenu();
            string selection = mainmenu.btnXbox

            string[] ListItemsArray = new string[11];
            lstGames.Items.CopyTo(ListItemsArray, 0);

            string selItem = lstGames.SelectedItem.ToString();

            picProductImg.SizeMode = PictureBoxSizeMode.StretchImage;

            if (selection == "xbox")
            {
                if (selItem == ListItemsArray[0])
                {
                    ChangeImage("forzahorizon.jpg");
                    lblProducttitle.Text = ListItemsArray[0];
                    lblPrice.Text = "£69.99";
                }
                else if (selItem == ListItemsArray[1])
                {
                    ChangeImage("unknownplayerground.jpg");
                    lblProducttitle.Text = ListItemsArray[1];
                }
                else if (selItem == ListItemsArray[2])
                {
                    ChangeImage("anthem.jpg");
                    lblProducttitle.Text = ListItemsArray[2];
                }
                else if (selItem == ListItemsArray[3])
                {
                    ChangeImage("crashbandicoot.jpg");
                    lblProducttitle.Text = ListItemsArray[3];
                }
                else if (selItem == ListItemsArray[4])
                {
                    ChangeImage("spyro.jpg");
                    lblProducttitle.Text = ListItemsArray[4];
                }
                else if (selItem == ListItemsArray[5])
                {
                    ChangeImage("fallenorder.jpeg");
                    lblProducttitle.Text = ListItemsArray[5];
                }
                else if (selItem == ListItemsArray[6])
                {
                    ChangeImage("battlefield.jpg");
                    lblProducttitle.Text = ListItemsArray[6];
                }
                else if (selItem == ListItemsArray[7])
                {
                    ChangeImage("battlefront.jpg");
                    lblProducttitle.Text = ListItemsArray[7];
                }
                else if (selItem == ListItemsArray[8])
                {
                    ChangeImage("division.jpg");
                    lblProducttitle.Text = ListItemsArray[8];
                }
                else if (selItem == ListItemsArray[9])
                {
                    ChangeImage("tomb.jpg");
                    lblProducttitle.Text = ListItemsArray[9];
                }
            }
            else
            {
                if (selItem == ListItemsArray[0])
                {
                    ChangeImage("thelastofus.png");
                    lblProducttitle.Text = ListItemsArray[0];
                }
                else if (selItem == ListItemsArray[1])
                {
                    ChangeImage("uncharted4.jfif");
                    lblProducttitle.Text = ListItemsArray[1];
                }
                else if (selItem == ListItemsArray[2])
                {
                    ChangeImage("godofwar.jpg");
                    lblProducttitle.Text = ListItemsArray[2];
                }
                else if (selItem == ListItemsArray[3])
                {
                    ChangeImage("ratchet.jpeg");
                    lblProducttitle.Text = ListItemsArray[3];
                }
                else if (selItem == ListItemsArray[4])
                {
                    ChangeImage("lbp3.jfif");
                    lblProducttitle.Text = ListItemsArray[4];
                }
                else if (selItem == ListItemsArray[5])
                {
                    ChangeImage("daysgone.jpg");
                    lblProducttitle.Text = ListItemsArray[5];
                }
                else if (selItem == ListItemsArray[6])
                {
                    ChangeImage("farcry.jpg");
                    lblProducttitle.Text = ListItemsArray[6];
                }
                else if (selItem == ListItemsArray[7])
                {
                    ChangeImage("spiderman.jpg");
                    lblProducttitle.Text = ListItemsArray[7];
                }
                else if (selItem == ListItemsArray[8])
                {
                    ChangeImage("cod.jpg");
                    lblProducttitle.Text = ListItemsArray[8];
                }
                else if (selItem == ListItemsArray[9])
                {
                    ChangeImage("darksouls.png");
                    lblProducttitle.Text = ListItemsArray[9];
                }
            }
        }

        private void ChangeImage(string image)
        {
            picProductImg.Image = Image.FromFile(@"D:\User\CPFin\Downloads\" + image);
        }
        
        
namespace Online_Shopping
{
    public partial class MainMenu : Form
    {
        public MainMenu()
        {
            InitializeComponent();
        }

        private void btnXbox_Click(object sender, EventArgs e)
        {
            lblSelection.Text = "xbox";
            Gamestore gamestore = new Gamestore(lblSelection.Text);
            this.Hide();
            gamestore.ShowDialog();
        }

        private void btnPlaystation_Click(object sender, EventArgs e)
        {
            Gamestore gamestore = new Gamestore(lblSelection.Text);
            lblSelection.Text = "playstation";
            this.Hide();
            gamestore.ShowDialog();
        }

        private void btnLogout_Click(object sender, EventArgs e)
        {
            this.Close();
        }


    }
}
