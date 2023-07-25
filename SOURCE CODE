/*
The following is the code to create a simple movie booking systrm
*/


#include<stdio.h>
#include<string.h>

void menu();
void admin();
void user();
void sign_up();
void sign_in();
void movie ();
void event ();
void nowstreaming ();
void comingsoon ();
void location();
void screen();
void transaction();
void snacks();
void db();

int i=1,at,ch, a_ch, u_ch,us_ch, m_ch, ns_ch,lt_ch,ns_ch,m,t_lt,time_lt,t_ns,time_ns,cs_ch,t,no_ticket,
e_ch,fi_ch,pkl_ch,ipl_ch,loc_ch,s_ch,be_ch,trans,n,f_i;

char rt='y',b='y',id[50],pass[50],ur_ticket[5],str[100],
fname[20]="test.txt",str1;

float s_price=0,ticket_price=200.00;
FILE * fptr;
  
struct User{
  char name[30];
  int phone_no;
  char U_name[30];
  char psd[20];
  int id;
  }U[50];

int main () {
  printf ("\n %15s WELCOME TO C-BOOK-KINGS %15s \n", " ", " ");
  menu();
  return 0;
}

void menu(){
  // MENU
  printf ("%18s ENTER 1 FOR ADMIN %17s \n", " ", " ");
  printf ("%18s ENTER 2 FOR USER %15s \n", " ", " ");
  printf ("\n");

  printf ("Enter your choice : ");
  scanf ("%d", &ch);

  switch (ch) {
    case 1:
    admin();
    break;

    case 2:
    printf("1. Sign up \n");
    printf("2. Sign in \n");
    printf("\n");
    printf("Enter your choice : ");
    scanf("%d",&us_ch);
    if(us_ch==1){
      sign_up();
    }
    
    else{
      sign_in(); 
    }
    break;

    default:
    break;
    }
}

void admin(){
  printf("Enter your id : ");
  scanf("%s", id);

    if (strcmp(id,"a123")==0) {
        while(rt=='y'|| rt=='Y' && at<=3) {
            printf("Enter your password : ");
            scanf("%s",pass);
    
            if (strcmp(pass,"admin")==0) {
              printf("\n %18s How can I help you \n", " ");
              printf("%13s Enter 1 to Edit price of the movie tickect \n", " ");
              printf("%13s Enter 2 to View reseved tickects \n", " ");
              printf("\n");

              printf("Enter your choice : ");
              scanf("%d", &a_ch);

              if(a_ch==1){
                printf("Enter the new price : Rs.");
                scanf("%d",&ticket_price);
                menu();
              }

              else if(a_ch==2){
                  fptr = fopen (fname, "r");  
	                printf("\n Reserved Seats :\n");
	                str1 = fgetc(fptr);
	                while (str1 != EOF){
			              printf ("%c", str1);
                    str1 = fgetc(fptr);
                  }
                printf("\n\n");
                fclose (fptr);     
                menu();
              }
              else {
                rt='n';
             }
            }
            
            else{
              printf("Incorrect Password \n");
                printf("Do you want to try again : ");
                scanf("%s",&rt);
                if(rt=='y' || rt=='Y'){
                at++;
                }
            }
        }
    }
    
    else{
        printf("You have entered an invalid user id");
        printf("Try again");
        admin();
    }
}

void user(){
    printf("\n %18s How can I help you \n", " ");
    printf("%13s Enter 1 to book movie tickets \n", " ");
    printf("%13s Enter 2 to book event tickets \n", " ");
    printf("%13s Enter 3 to Exit User \n", " ");
    printf("\n");

    printf("Enter your choice : ");
    scanf("%d", &u_ch);

    switch (u_ch) {
    case 1:
      movie(); 
      break;

    case 2:
      event(); 
      break;
    }
  }
  

void sign_up(){
  
  printf("ENTER YOUR NAME : ");
  scanf("%s",U[i].name);
  printf("ENTER YOUR PHONE NUMBER : ");
  scanf("%d",&U[i].phone_no);
  printf("ENTER YOUR USERNAME : ");
  scanf("%s",U[i].U_name);
  printf("ENTER YOUR PASSWORD : ");
  scanf("%s",U[i].psd);
  printf("YOUR ID IS %d \n",i);
  i++;
                         
  printf("\nYOUR ACCOUNT HAS BEEN CREATED \n");
  sign_in();
 }

void sign_in(){
  int a;
  char U_name1[30],psd1[20];
  printf("ENTER YOUR USERNAME : ");
  scanf("%s",U_name1);
  printf("ENTER YOUR PASSWORD : ");
  scanf("%s",psd1);
  printf("ENTER YOUR ID : ");
  scanf("%d",&a);
  if(strcmp(U[a].U_name,U_name1)==0&&strcmp(U[a].psd,psd1)==0){
    printf("SIGNED IN SUCCESSFULLY \n");
    user();
  }
  else{
    printf("Try Again \n");
    sign_in();
  }
}

void movie(){
    printf("\n");
    printf("MENU \n");
    printf("1. Now Streaming \n");
    printf("2. Coming Soon \n");
    printf("\n");
    
    printf("Enter your choice : ");
    scanf("%d",&m_ch);
    
    if(m_ch == 1){
      nowstreaming();
    }
    else if(m_ch == 0){
      comingsoon();
    }
    
}

void nowstreaming(){
    
    printf("Now Streaming Movies List \n");
    printf("1. Avatar: Way of water \n");
    printf("2. Naai Sekar Returns \n");
    printf("\n");
    
    printf("Choose a movie : ");
    scanf("%d",&m);
    
    if(m==1) {
        printf("Menu \n");
        printf("1. Book Tickets \n");
        printf("2. Reviews \n");
        printf("3. Main Cast \n");
        printf("\n");
        
        printf("Enter your choice : ");
        scanf("%d",&lt_ch); 
        
            if(lt_ch==1) {   
	             
                location();
                printf("\n");
                printf("Select The Theatre \n");
                printf("1.Theatre A \n");
                printf("2.Theatre B \n");
                printf("\n");
                  
                printf("Choose a theatre for Avatar: Way of water:");
                scanf("%d",&t_lt);
                  
                if(t_lt==1){  
                    printf("Show timings for Avatar: Way of water \n");
                    printf("1. Morning Show \n");
                    printf("2. Afternoon Show \n");
                    printf("\n");
                              
                    printf("Enter your choice : ");
                    scanf("%d",&time_lt);
                    if(time_lt==1) {
	                    printf("WELCOME TO Avatar: Way of water'S MORNING SHOW IN THEATRE A \n");
	                    screen();
	                    }
                        else {
                        printf("WELCOME TO Avatar: Way of water'S AFTERNOON SHOW IN THEATRE A \n");
                        screen();
                        }
	            }
	            
                else if(t_lt==2) {
                    printf("Show timings for Avatar: Way of water \n");
                    printf("1. Morning Show \n");
                    printf("2. Afternoon Show \n");
                    printf("3. Evening Show \n");
                    printf("\n");
                              
                    printf("Enter your choice : ");
                    scanf("%d",&time_lt);
                    if(time_lt==1) {
                        printf("WELCOME TO Avatar: Way of water'S MORNING SHOW IN THEATRE B \n");
	                    screen();
	                }
                    else if(time_lt==2) {
                        printf("WELCOME TO Avatar: Way of water'S AFTERNOON SHOW IN THEATRE B \n");
                        screen();
	                }
	                else{
	                    printf("WELCOME TO Avatar: Way of water'S EVENING SHOW IN THEATRE B \n");
	                    screen();
                    }
	            }
            }
              
      else if(lt_ch == 2){
        printf("REVIEW \n");
        printf("78 percent by Rotten Tomatoes \n");
        printf(" 8/10 by IGN \n ");
        printf("8/10 by IMDb \n");
        printf("Audience Rating : 4.5(21088 rating) \n");
        printf("\n");
        nowstreaming();
        }
        
      else{
        printf("MAIN CAST \n");
        printf("Sam Worthington as Jake Sully \n");
        printf("Zoe Saldaña as Neytiri \n");
        printf("Jamie Flatters as Neteyam \n");
        printf("\n");
        nowstreaming();
      }
      
    }
      
    else if(m==2) {
        printf("Menu \n");
        printf("1. Book Tickets \n");
        printf("2. Reviews \n");
        printf("3. Main Cast \n");
        printf("\n");
        
        printf("Enter your choice : ");
        scanf("%d",&ns_ch); 
        
            if(ns_ch==1) {   
	             
                location();
                printf("Select The Theatre");
                printf("1.Theatre A \n");
                printf("2.Theatre B \n");
                printf("\n");
                  
                printf("Choose a theatre for NAAI SEKAR RETURNS : ");
                scanf("%d",&t_ns);
                  
                if(t_ns==1){    
                    printf("Show timings for NAAI SEKAR RETURNS \n");
                    printf("1. Early Morning Show \n");
                    printf("2. Morning Show \n");
                    printf("3. Afternoon Show \n");
                    printf("4. Evening Show \n");
                    printf("5. Nigth Show \n");
                    printf("\n");
                              
                    printf("Enter your choice : ");
                    scanf("%d",&time_ns);
                    
                    switch(time_ns){
                        case 1:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S EARLY MORNING SHOW IN THEATRE A \n");
                        screen();
                        break;
                        case 2:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S MORNING SHOW IN THEATRE A \n");
                        screen();
                        break;
                        case 3:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S AFTERNOON SHOW IN THEATRE A \n");
                        screen();
                        break;
                        case 4:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S EVENING SHOW IN THEATRE A \n");
                        screen();
                        break;
                        case 5:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S NIGHT SHOW IN THEATRE A \n");
                        screen();
                        break;
                        default:
                        break;
                        
                    }
                  }
                   
                else{      
                    printf("Show timings for Love Today \n");
                    printf("1. Early Morning Show \n");
                    printf("2. Morning Show \n");
                    printf("3. Afternoon Show \n");
                    printf("4. Evening Show \n");
                    printf("5. Nigth Show \n");
                    printf("\n");
                              
                    printf("Enter your choice : ");
                    scanf("%d",&time_lt);
                    
                    switch(time_lt){
                        case 1:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S EARLY MORNING SHOW IN THEATRE B \n");
                        screen();
                        break;
                        case 2:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S MORNING SHOW IN THEATRE B \n");
                        screen();
                        break;
                        case 3:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S AFTERNOON SHOW IN THEATRE B \n");
                        screen();
                        break;
                        case 4:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S EVENING SHOW IN THEATRE B \n");
                        screen();
                        break;
                        case 5:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S NIGHT SHOW IN THEATRE B \n");
                        screen();
                        break;
                        default:
                        break;
                        
                    }                   
	             }
            }
      else if(ns_ch == 2){
        printf("REVIEW \n");
        printf("2.5/5 by Times of India \n");
        printf("5.9/10 by IMDb \n");
        printf("1/5 by The Newa Minute \n");
        printf("Audience rating : 4.2(334 rating) \n");
      }
      else{
        printf("MAIN CAST \n");
        printf("Vadivelu as Naai Sekar \n");
        printf("Shivani Narayanan as Bobby \n");
        printf("Sivaangi as Surangani \n");
      }
    }
  else{
    printf("Enter 1 or 2 ");
    nowstreaming();
    }
  }

void comingsoon(){
  printf("MENU"); 
  printf("1. View up coming \n");
  printf("2. Go to now streaming \n");
  printf("Enter your choice : ");
  scanf("%d",&cs_ch);
  if(cs_ch==1){
    printf("Coming soon movies are \n");
    printf("1. VARISU \n");
    printf("2. THUNIVU \n");
    printf("\n");
    printf("Enter ur choice:");
    scanf("%d",&t);
        if(cs_ch==1)
            {
                printf("\n Movie name: VARISU \n");
                printf("Release date: 12th January 2023 \n");
                printf("Booking opens on 27th December 2022 \n");
                printf("Category: Action + Drama ");
                printf("Overview : \n");
                printf("Vijay Rajendran is a happy to-go lucky man. Things change when his foster father dies unexpectedly.");
                printf("Director : Vamshi");
                printf("Main Cast : Vijay , Rashmika , Shaam ");
                
            }
        else
            {
                printf("\n Movie name: THUNIVU \n");
                printf("Release date: 12th January 2023 \n");
                printf("Booking opens on  29 December 2022 \n");
                printf("Category: Action + Adventure + Thriller ");
                printf("Overview : \n");
                printf("A mysterious mastermind and his team forms a plan and commits bank heists across Chennai, but their motive of the heists remains mysterious.");
                printf("Director : H Vinoth");
                printf("Main Cast : Ajith , Manju Warrier ");             
            }
  }
  else{
    nowstreaming();
  }
}
    
void event(){
  int a_row,b_row,t_price;
  printf("MENU \n");
  printf("1. FIFA WORLD CUP \n");
  printf("2. PKL Finals \n");
  printf("3. IPL Action \n");
  printf("\n");
  printf("Enter your choice : ");
  scanf("%d",&e_ch);

  if(e_ch==1){
    printf("Welcome to fifa world cup finals \n");
    printf("1. Book Ticket \n");
    printf("2. Overview \n");
    printf("Enter your choice : ");
    scanf("%d",&fi_ch);

    if(fi_ch==1){
      printf("Finals : Argentina Vs France \n");
      printf("Date : 18th December 2022 \n");
      printf("Time : 8:30 IST \n");
      printf("Venue : Lusail Stadium, QATAR \n");
      printf("Category A ticket :");
      printf(" Rs.48000/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Category B ticket :");
      printf("Rs.16000/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Enter number of Category A and Category B tickets:");
      scanf("%d%d",&a_row,&b_row);
      t_price=(48000*a_row)+(16000*b_row);
      printf("\nYou have to pay : Rs. %d/-",t_price);
      transaction();
    }
    else{
      printf("Who will win the 2022 world cup !!! \n");
      printf("Will MBappe Stikes again and get two world cup in a row or Will Messi show who is the real GOAT before he goes \n");
    }
  }

  else if(e_ch==2){
    printf("Welcome to PKL finals \n");
    printf("1. Book Ticket \n");
    printf("2. Overview \n");
    printf("Enter your choice : ");
    scanf("%d",&pkl_ch);

    if(pkl_ch==1){
      printf("Finals : Jaipur Pink Panthers Vs Punari Paltans \n");
      printf("Date : 17th December 2022 \n");
      printf("Time : 8:30 IST \n");
      printf("Venue : Mumbai \n");
      printf("Category A ticket :");
      printf(" Rs.8000/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Category B ticket :");
      printf("Rs.500/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Enter number of Category A and Category B tickets:");
      scanf("%d%d",&a_row,&b_row);
      t_price=(8000*a_row)+(500*b_row);
      printf("\nYou have to pay : Rs. %d/-",t_price);
      transaction();
    }
    else{
      printf("Who will lift the pkl cup season 9 !!! \n");
      printf("Will the pink panthers roar or Will Fazel Sulthan show who is the sulthan and tackel Panthers \n");
    }
  }
  
  else{
    printf("Welcome to IPL Mini action \n");
    printf("1. Book Ticket \n");
    printf("2. Overview \n");
    printf("Enter your choice : ");
    scanf("%d",&ipl_ch);

    if(ipl_ch==1){
      printf("Date : 23th December 2022 \n");
      printf("Time : 2:30 IST \n");
      printf("Venue : Kochi \n");
      printf("Category A ticket :");
      printf(" Rs.5000/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Category B ticket :");
      printf("Rs.500/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Enter number of Category A and Category B tickets:");
      scanf("%d%d",&a_row,&b_row);
      t_price=(5000*a_row)+(500*b_row);
      printf("\nYou have to pay : Rs. %d/-",t_price);
      transaction();
    }
    else{
      printf("Who gonna smack the hammer !!! \n");
      printf("There is going to be all-rounder fight between tems \n");
    }
  }  
}  

void screen(){
 
  printf("CHOOSE YOUR CONFORTABLE SEAT \n");
  printf("\n\n");
  printf(" A 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" B 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" C 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" D 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" E 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" F 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf("\n");
  printf(" G 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" I 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" J 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" K 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" L 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf("\n\n");
  printf("%30s SCREEN \n " , " ");
  
  fptr = fopen (fname, "r");  
	printf("\n Already Reserved Seats :\n");
	str1 = fgetc(fptr);
	while (str1 != EOF)
		{
			printf ("%c", str1);
			str1 = fgetc(fptr);
		}
    printf("\n\n");
    fclose (fptr);
  
	printf("Enter the number of seats you want to book: ");
	scanf("%d", &n);
  printf("Enter your seats : \n");
	fptr = fopen (fname,"a"); 
	for(f_i = 0; f_i < n+1;f_i++)
		{
		fgets(str, sizeof str, stdin);
		fputs(str, fptr);
		}
  fclose (fptr);

  s_price=s_price+ (n*ticket_price);
  
  snacks();
 
}

void snacks(){
int size,s_size,m_size,l_size,c_q,f_q,sn_ch,sp_size,mp_size,lp_size,p_q,c_ch,c1_q,c2_q;
    char r;
    printf("--SNACKS TIME--\n");
    printf("MENU \n");
    printf("1. BEVERAGES \n");
    printf("2. SNACKS \n");
    printf("3. COMBO \n");
    printf("4. NO SNACKS \n");
    printf("\n");
     
    printf("Enter your choice : ");
    scanf("%d",&s_ch);
    switch(s_ch){
      case 1:
        printf("Select your favorite Beverage \n");
        printf("COKE         Rs.80-150 \n");
        printf("COLD COFFEE  Rs.200 \n");
        printf("FRESH JUICE  Rs.160 \n");
        printf("\n");
        printf("Enter Your Choice : ");
        scanf("%d",&be_ch);

      if(be_ch==1){
        printf("ENTER THE SIZE : ");
        printf("1-Small     Rs.80/- \n");
        printf("2-Medium    Rs.100/- \n");
        printf("3-Large     Rs.150/- \n");
        printf("\n");
        printf("Enter number of drinks of small/medium/large : ");
        scanf("%d%d%d",&s_size,&m_size,&l_size);
        s_price= s_price + (80*s_size)+(100*m_size)+(150*l_size);
        }
      else if(be_ch==2){
        printf("Enter the quantity : ");
        scanf("%d",&c_q);
        s_price = s_price + (200*c_q);
      }
      else{
        printf("Enter the quantity : ");
        scanf("%d",&f_q);
        s_price = s_price + (160*f_q);
      }
      printf("Do your want to add more snacks (Y/N): ");
      scanf("%s",&r);
      if(r=='y'||r=='Y'){
        snacks();
      }
      else{
        break;
      }

      case 2:
        printf("Select your favorite Snacks \n");
        printf("POPCORN         Rs.150-300/- \n");
        printf("PUFFS           Rs.60/- \n");
        printf("\n");
        printf("Enter Your Choice : ");
        scanf("%d",&sn_ch);

      if(sn_ch==1){
        printf("ENTER THE SIZE : ");
        printf("1-Small     Rs.150/- \n");
        printf("2-Medium    Rs.200/- \n");
        printf("3-Large     Rs.300/- \n");
        printf("\n");
        printf("Enter number of popcorn of small/medium/large : ");
        scanf("%d%d%d",&sp_size,&mp_size,&lp_size);
        s_price= s_price + (150*sp_size)+(200*mp_size)+(300*lp_size);
        }
      else{
        printf("Enter the quantity : ");
        scanf("%d",&p_q);
        s_price = s_price + (60*p_q);
      }
      printf("Do your want to add more snacks (Y/N): ");
      scanf("%s",&r);
      if(r=='y'||r=='Y'){
        snacks();
      }
      else {
        break;
      }

      case 3:
      printf("Enter your favirote combo \n");
      printf("1. M-POPCORN + L-COKE Rs.250/- \n");
      printf("2. PUFFS + M-COKE     Rs.150/- \n");
      printf("\n");
      printf("Enter your choice : ");
      scanf("%d",&c_ch);
      if(c_ch==1){
        printf("Enter the quantity : ");
        scanf("%d",&c1_q);
        s_price = s_price + (250*c1_q);
      }
      else{
        printf("Enter the quantity : ");
        scanf("%d",&c2_q);
        s_price = s_price + (150*c2_q);
      }
      printf("Do your want to add more snacks (Y/N): ");
      scanf("%s",&r);
      if(r=='y'||r=='Y'){
        snacks();
      }
      else{
        break;
      }

      case 4:
      break;

      default:
        printf("Enter a number between 1-4");
        snacks();
  }
 printf("You should pay : Rs.%2f/- ",s_price);
 transaction();
}

void location(){
	printf("Available locations nearby \n");
	printf("1. Adyar \n");
  printf("2. OMR \n");
  printf("3. ECR \n");
  printf("4. Kelambakkam \n");
  printf("\n");
	printf("Enter your location:");
	scanf("%d",&loc_ch);
  
	printf("\nThe available theatres are : \n");
	if(loc_ch==1)
	 {
	   printf("Theatre A is 3km from your location \n");
	   printf("Theatre B is 7km from your location \n");
    }
  else if(loc_ch==2)
	 {
	   printf("Theatre A is 8km from your location \n");
	   printf("Theatre B is 2km from your location \n");
    }
  else if(loc_ch==3)
    {
	   printf("Theatre A is 1km from your location \n");
	   printf("Theatre B is 5km from your location \n");
    }
	else if(loc_ch==4)
	 {
	   printf("Theatre A is 6km from your location \n");
	   printf("Theatre B is 12km from your location \n");
	 }
	 else
	   printf("Invalid location \n");
  }

void transaction(){
  printf("Your total bill %2f",)
  printf("How you like to proceed transaction \n");
  printf(" 1. Debit card \n");
  printf(" 2. Credit card \n");
  printf("\n");
  printf("\nEnter your mode of transaction:");
  scanf("%d",&trans);
  if(trans==1){
    printf("DEBIT CARD TRANSACTION \n");
    db();
  }
  else{
    printf("CREDIT CARD TRANSACTION \n");
    db();
  }
}

void db(){
  char sname[100],sno[30],otp[4];
  int mon,year,cvv;

  printf(".......... TRANSACTION........ \n");
  printf("Enter name as it appears on your card : ");
  scanf("%s",sname);
  printf("Enter your card number : ");
  scanf("%s",sno);
  printf("Enter expiry date(month&year) : ");
  scanf("%d %d",&mon,&year);
  printf("\n");
  
  printf("Enter CVV : ");
  scanf("%d",&cvv);
  if(strlen(cvv)==3){
    printf("Enter your OTP number:");
    scanf("%s",otp);
    if(strlen(otp)==4){
      printf("YOUR TRANSACTION HAS BEEN DONE SUCCESSFULLY \n");
      printf("YOUR TICKET IS BOOKED \n");
    }
    else{
      printf("YOUR TRANSACTION FAILED TRY AGAIN \n");
      transaction();
    }
  }
  else{
    printf("YOUR TRANSACTION FAILED TRY AGAIN \n");
    transaction();
  }
}SOURCE CODE : 
 #include<stdio.h>
#include<string.h>

void menu();
void admin();
void user();
void sign_up();
void sign_in();
void movie ();
void event ();
void nowstreaming ();
void comingsoon ();
void location();
void screen();
void transaction();
void snacks();
void db();

int i=1,at,ch, a_ch, u_ch,us_ch, m_ch, ns_ch,lt_ch,ns_ch,m,t_lt,time_lt,t_ns,time_ns,cs_ch,t,no_ticket,
e_ch,fi_ch,pkl_ch,ipl_ch,loc_ch,s_ch,be_ch,trans,ticket_price=200,n,f_i;

char rt='y',b='y',id[50],pass[50],ur_ticket[5],str[100],
fname[20]="test.txt",str1;

float s_price=0;

FILE * fptr;
  
struct User{
  char name[30];
  int phone_no;
  char U_name[30];
  char psd[20];
  int id;
  }U[50];

int main () {
  printf ("\n %15s WELCOME TO C-BOOK-KINGS %15s \n", " ", " ");
  menu();
  return 0;
}

void menu(){
  // MENU
  printf ("%18s ENTER 1 FOR ADMIN %17s \n", " ", " ");
  printf ("%18s ENTER 2 FOR USER %15s \n", " ", " ");
  printf ("\n");

  printf ("Enter your choice : ");
  scanf ("%d", &ch);

  switch (ch) {
    case 1:
    admin();
    break;

    case 2:
    printf("1. Sign up \n");
    printf("2. Sign in \n");
    printf("\n");
    printf("Enter your choice : ");
    scanf("%d",&us_ch);
    if(us_ch==1){
      sign_up();
    }
    
    else{
      sign_in(); 
    }
    break;

    default:
    break;
    }
}

void admin(){
  printf("Enter your id : ");
  scanf("%s", id);

    if (strcmp(id,"a123")==0) {
        while(rt=='y'|| rt=='Y' && at<=3) {
            printf("Enter your password : ");
            scanf("%s",pass);
    
            if (strcmp(pass,"admin")==0) {
              printf("\n %18s How can I help you \n", " ");
              printf("%13s Enter 1 to Edit price of the movie tickect \n", " ");
              printf("%13s Enter 2 to View reseved tickects \n", " ");
              printf("\n");

              printf("Enter your choice : ");
              scanf("%d", &a_ch);

              if(a_ch==1){
                printf("Enter the new price : Rs.");
                scanf("%d",&ticket_price);
                menu();
              }

              else if(a_ch==2){
                  fptr = fopen (fname, "r");  
	                printf("\n Reserved Seats :\n");
	                str1 = fgetc(fptr);
	                while (str1 != EOF){
			              printf ("%c", str1);
                    str1 = fgetc(fptr);
                  }
                printf("\n\n");
                fclose (fptr);     
                menu();
              }
              else {
                rt='n';
             }
            }
            
            else{
              printf("Incorrect Password \n");
                printf("Do you want to try again : ");
                scanf("%s",&rt);
                if(rt=='y' || rt=='Y'){
                at++;
                }
            }
        }
    }
    
    else{
        printf("You have enetred an invalid user id");
        printf("Try again");
        admin();
    }
}

void user(){
    printf("\n %18s How can I help you \n", " ");
    printf("%13s Enter 1 to book movie tickect \n", " ");
    printf("%13s Enter 2 to book event tickects \n", " ");
    printf("%13s Enter 3 to Exit User \n", " ");
    printf("\n");

    printf("Enter your choice : ");
    scanf("%d", &u_ch);

    switch (u_ch) {
    case 1:
      movie(); 
      break;

    case 2:
      event(); 
      break;
    }
  }
  

void sign_up(){
  
  printf("ENTER YOUR NAME : ");
  scanf("%s",U[i].name);
  printf("ENTER YOUR PHONE NUMBER : ");
  scanf("%d",&U[i].phone_no);
  printf("ENTER YOUR USERNAME : ");
  scanf("%s",U[i].U_name);
  printf("ENTER YOUR PASSWORD : ");
  scanf("%s",U[i].psd);
  printf("YOUR ID IS %d \n",i);
  i++;
                         
  printf("\nYOUR ACCOUNT HAS BEEN CREATED \n");
  sign_in();
 }

void sign_in(){
  int a;
  char U_name1[30],psd1[20];
  printf("ENTER YOUR USERNAME : ");
  scanf("%s",U_name1);
  printf("ENTER YOUR PASSWORD : ");
  scanf("%s",psd1);
  printf("ENTER YOUR ID : ");
  scanf("%d",&a);
  if(strcmp(U[a].U_name,U_name1)==0&&strcmp(U[a].psd,psd1)==0){
    printf("SIGNED IN SUCCESSFULLY \n");
    user();
  }
  else{
    printf("Try Again \n");
    sign_in();
  }
}

void movie(){
    printf("\n");
    printf("MENU \n");
    printf("1. Now Streaming \n");
    printf("2. Coming Soon \n");
    printf("\n");
    
    printf("Enter your choice : ");
    scanf("%d",&m_ch);
    
    if(m_ch == 1){
      nowstreaming();
    }
    else if(m_ch == 0){
      comingsoon();
    }
    
}

void nowstreaming(){
    
    printf("Now Streaming Movies List \n");
    printf("1. Avatar: Way of water \n");
    printf("2. Naai Sekar Returns \n");
    printf("\n");
    
    printf("Choose a movie : ");
    scanf("%d",&m);
    
    if(m==1) {
        printf("Menu \n");
        printf("1. Book Tickets \n");
        printf("2. Reviews \n");
        printf("3. Main Cast \n");
        printf("\n");
        
        printf("Enter your choice : ");
        scanf("%d",&lt_ch); 
        
            if(lt_ch==1) {   
	             
                location();
                printf("\n");
                printf("Select The Theatre \n");
                printf("1.Theatre A \n");
                printf("2.Theatre B \n");
                printf("\n");
                  
                printf("Choose a theatre for Avatar: Way of water:");
                scanf("%d",&t_lt);
                  
                if(t_lt==1){  
                    printf("Show timings for Avatar: Way of water \n");
                    printf("1. Morning Show \n");
                    printf("2. Afternoon Show \n");
                    printf("\n");
                              
                    printf("Enter your choice : ");
                    scanf("%d",&time_lt);
                    if(time_lt==1) {
	                    printf("WELCOME TO Avatar: Way of water'S MORNING SHOW IN THEATRE A \n");
	                    screen();
	                    }
                        else {
                        printf("WELCOME TO Avatar: Way of water'S AFTERNOON SHOW IN THEATRE A \n");
                        screen();
                        }
	            }
	            
                else if(t_lt==2) {
                    printf("Show timings for Avatar: Way of water \n");
                    printf("1. Morning Show \n");
                    printf("2. Afternoon Show \n");
                    printf("3. Evening Show \n");
                    printf("\n");
                              
                    printf("Enter your choice : ");
                    scanf("%d",&time_lt);
                    if(time_lt==1) {
                        printf("WELCOME TO Avatar: Way of water'S MORNING SHOW IN THEATRE B \n");
	                    screen();
	                }
                    else if(time_lt==2) {
                        printf("WELCOME TO Avatar: Way of water'S AFTERNOON SHOW IN THEATRE B \n");
                        screen();
	                }
	                else{
	                    printf("WELCOME TO Avatar: Way of water'S EVENING SHOW IN THEATRE B \n");
	                    screen();
                    }
	            }
            }
              
      else if(lt_ch == 2){
        printf("REVIEW \n");
        printf("78 percent by Rotten Tomatoes \n");
        printf(" 8/10 by IGN \n ");
        printf("8/10 by IMDb \n");
        printf("Audience Rating : 4.5(21088 rating) \n");
        printf("\n");
        nowstreaming();
        }
        
      else{
        printf("MAIN CAST \n");
        printf("Sam Worthington as Jake Sully \n");
        printf("Zoe Saldaña as Neytiri \n");
        printf("Jamie Flatters as Neteyam \n");
        printf("\n");
        nowstreaming();
      }
      
    }
      
    else if(m==2) {
        printf("Menu \n");
        printf("1. Book Tickets \n");
        printf("2. Reviews \n");
        printf("3. Main Cast \n");
        printf("\n");
        
        printf("Enter your choice : ");
        scanf("%d",&ns_ch); 
        
            if(ns_ch==1) {   
	             
                location();
                printf("Select The Theatre");
                printf("1.Theatre A \n");
                printf("2.Theatre B \n");
                printf("\n");
                  
                printf("Choose a theatre for NAAI SEKAR RETURNS : ");
                scanf("%d",&t_ns);
                  
                if(t_ns==1){    
                    printf("Show timings for NAAI SEKAR RETURNS \n");
                    printf("1. Early Morning Show \n");
                    printf("2. Morning Show \n");
                    printf("3. Afternoon Show \n");
                    printf("4. Evening Show \n");
                    printf("5. Nigth Show \n");
                    printf("\n");
                              
                    printf("Enter your choice : ");
                    scanf("%d",&time_ns);
                    
                    switch(time_ns){
                        case 1:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S EARLY MORNING SHOW IN THEATRE A \n");
                        screen();
                        break;
                        case 2:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S MORNING SHOW IN THEATRE A \n");
                        screen();
                        break;
                        case 3:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S AFTERNOON SHOW IN THEATRE A \n");
                        screen();
                        break;
                        case 4:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S EVENING SHOW IN THEATRE A \n");
                        screen();
                        break;
                        case 5:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S NIGHT SHOW IN THEATRE A \n");
                        screen();
                        break;
                        default:
                        break;
                        
                    }
                  }
                   
                else{      
                    printf("Show timings for Love Today \n");
                    printf("1. Early Morning Show \n");
                    printf("2. Morning Show \n");
                    printf("3. Afternoon Show \n");
                    printf("4. Evening Show \n");
                    printf("5. Nigth Show \n");
                    printf("\n");
                              
                    printf("Enter your choice : ");
                    scanf("%d",&time_lt);
                    
                    switch(time_lt){
                        case 1:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S EARLY MORNING SHOW IN THEATRE B \n");
                        screen();
                        break;
                        case 2:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S MORNING SHOW IN THEATRE B \n");
                        screen();
                        break;
                        case 3:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S AFTERNOON SHOW IN THEATRE B \n");
                        screen();
                        break;
                        case 4:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S EVENING SHOW IN THEATRE B \n");
                        screen();
                        break;
                        case 5:
                        printf("WELCOME TO NAAI SEKAR RETURNS'S NIGHT SHOW IN THEATRE B \n");
                        screen();
                        break;
                        default:
                        break;
                        
                    }                   
	             }
            }
      else if(ns_ch == 2){
        printf("REVIEW \n");
        printf("2.5/5 by Times of India \n");
        printf("5.9/10 by IMDb \n");
        printf("1/5 by The Newa Minute \n");
        printf("Audience rating : 4.2(334 rating) \n");
      }
      else{
        printf("MAIN CAST \n");
        printf("Vadivelu as Naai Sekar \n");
        printf("Shivani Narayanan as Bobby \n");
        printf("Sivaangi as Surangani \n");
      }
    }
  else{
    printf("Enter 1 or 2 ");
    nowstreaming();
    }
  }

void comingsoon(){
  printf("MENU"); 
  printf("1. View up coming \n");
  printf("2. Go to now streaming \n");
  printf("Enter your choice : ");
  scanf("%d",&cs_ch);
  if(cs_ch==1){
    printf("Coming soon movies are \n");
    printf("1. VARISU \n");
    printf("2. THUNIVU \n");
    printf("\n");
    printf("Enter ur choice:");
    scanf("%d",&t);
        if(cs_ch==1)
            {
                printf("\n Movie name: VARISU \n");
                printf("Release date: 12th January 2023 \n");
                printf("Booking opens on 27th December 2022 \n");
                printf("Category: Action + Drama ");
                printf("Overview : \n");
                printf("Vijay Rajendran is a happy to-go lucky man. Things change when his foster father dies unexpectedly.");
                printf("Director : Vamshi");
                printf("Main Cast : Vijay , Rashmika , Shaam ");
                
            }
        else
            {
                printf("\n Movie name: THUNIVU \n");
                printf("Release date: 12th January 2023 \n");
                printf("Booking opens on  29 December 2022 \n");
                printf("Category: Action + Adventure + Thriller ");
                printf("Overview : \n");
                printf("A mysterious mastermind and his team forms a plan and commits bank heists across Chennai, but their motive of the heists remains mysterious.");
                printf("Director : H Vinoth");
                printf("Main Cast : Ajith , Manju Warrier ");             
            }
  }
  else{
    nowstreaming();
  }
}
    
void event(){
  int a_row,b_row,t_price;
  printf("MENU \n");
  printf("1. FIFA WORLD CUP \n");
  printf("2. PKL Finals \n");
  printf("3. IPL Action \n");
  printf("\n");
  printf("Enter your choice : ");
  scanf("%d",&e_ch);

  if(e_ch==1){
    printf("Welcome to fifa world cup finals \n");
    printf("1. Book Ticket \n");
    printf("2. Overview \n");
    printf("Enter your choice : ");
    scanf("%d",&fi_ch);

    if(fi_ch==1){
      printf("Finals : Argentina Vs France \n");
      printf("Date : 18th December 2022 \n");
      printf("Time : 8:30 IST \n");
      printf("Venue : Lusail Stadium, QATAR \n");
      printf("Category A ticket :");
      printf(" Rs.48000/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Category B ticket :");
      printf("Rs.16000/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Enter number of Category A and Category B tickets:");
      scanf("%d%d",&a_row,&b_row);
      t_price=(48000*a_row)+(16000*b_row);
      printf("\nYou have to pay : Rs. %d/-",t_price);
      transaction();
    }
    else{
      printf("Who will win the 2022 world cup !!! \n");
      printf("Will MBappe Stikes again and get two world cup in a row or Will Messi show who is the real GOAT before he goes \n");
    }
  }

  else if(e_ch==2){
    printf("Welcome to PKL finals \n");
    printf("1. Book Ticket \n");
    printf("2. Overview \n");
    printf("Enter your choice : ");
    scanf("%d",&pkl_ch);

    if(pkl_ch==1){
      printf("Finals : Jaipur Pink Panthers Vs Punari Paltans \n");
      printf("Date : 17th December 2022 \n");
      printf("Time : 8:30 IST \n");
      printf("Venue : Mumbai \n");
      printf("Category A ticket :");
      printf(" Rs.8000/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Category B ticket :");
      printf("Rs.500/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Enter number of Category A and Category B tickets:");
      scanf("%d%d",&a_row,&b_row);
      t_price=(8000*a_row)+(500*b_row);
      printf("\nYou have to pay : Rs. %d/-",t_price);
      transaction();
    }
    else{
      printf("Who will lift the pkl cup season 9 !!! \n");
      printf("Will the pink panthers roar or Will Fazel Sulthan show who is the sulthan and tackel Panthers \n");
    }
  }
  
  else{
    printf("Welcome to IPL Mini action \n");
    printf("1. Book Ticket \n");
    printf("2. Overview \n");
    printf("Enter your choice : ");
    scanf("%d",&ipl_ch);

    if(ipl_ch==1){
      printf("Date : 23th December 2022 \n");
      printf("Time : 2:30 IST \n");
      printf("Venue : Kochi \n");
      printf("Category A ticket :");
      printf(" Rs.5000/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Category B ticket :");
      printf("Rs.500/- \n");
      printf("Each ticket grants entry to 1 person. \n");
      printf("Enter number of Category A and Category B tickets:");
      scanf("%d%d",&a_row,&b_row);
      t_price=(5000*a_row)+(500*b_row);
      printf("\nYou have to pay : Rs. %d/-",t_price);
      transaction();
    }
    else{
      printf("Who gonna smack the hammer !!! \n");
      printf("There is going to be all-rounder fight between tems \n");
    }
  }  
}  

void screen(){
 
  printf("CHOOSE YOUR CONFORTABLE SEAT \n");
  printf("\n\n");
  printf(" A 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" B 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" C 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" D 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" E 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" F 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf("\n");
  printf(" G 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" I 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" J 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" K 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf(" L 1 2 3 4 5 \t  6 7 8 9 10 11 12 13 14 15 16 17 18 \t 19 20 21 22 23 \n");
  printf("\n\n");
  printf("%30s SCREEN \n " , " ");
  
  fptr = fopen (fname, "r");  
	printf("\n Already Reserved Seats :\n");
	str1 = fgetc(fptr);
	while (str1 != EOF)
		{
			printf ("%c", str1);
			str1 = fgetc(fptr);
		}
    printf("\n\n");
    fclose (fptr);
  
	printf("Enter the number of seats you want to book: ");
	scanf("%d", &n);
  printf("Enter your seats : \n");
	fptr = fopen (fname,"a"); 
	for(f_i = 0; f_i < n+1;f_i++)
		{
		fgets(str, sizeof str, stdin);
		fputs(str, fptr);
		}
  fclose (fptr);

  s_price=s_price+ (n*ticket_price);
  
  snacks();
 
}

void snacks(){
    int size,s_size,m_size,l_size,c_q,f_q,sn_ch,sp_size,mp_size,lp_size,p_q,c_ch,c1_q,c2_q;
    char r;
    printf("--SNACKS TIME--\n");
    printf("MENU \n");
    printf("1. BEVERAGES \n");
    printf("2. SNACKS \n");
    printf("3. COMBO \n");
    printf("4. NO SNACKS \n");
    printf("\n");
     
    printf("Enter your choice : ");
    scanf("%d",&s_ch);
    switch(s_ch){
      case 1:
        printf("Select your favorite Beverage \n");
        printf("COKE         Rs.80-150 \n");
        printf("COLD COFFEE  Rs.200 \n");
        printf("FRESH JUICE  Rs.160 \n");
        printf("\n");
        printf("Enter Your Choice : ");
        scanf("%d",&be_ch);

      if(be_ch==1){
        printf("ENTER THE SIZE : ");
        printf("1-Small     Rs.80/- \n");
        printf("2-Medium    Rs.100/- \n");
        printf("3-Large     Rs.150/- \n");
        printf("\n");
        printf("Enter number of drinks of small/medium/large : ");
        scanf("%d%d%d",&s_size,&m_size,&l_size);
        s_price= s_price + (80*s_size)+(100*m_size)+(150*l_size);
        }
      else if(be_ch==2){
        printf("Enter the quantity : ");
        scanf("%d",&c_q);
        s_price = s_price + (200*c_q);
      }
      else{
        printf("Enter the quantity : ");
        scanf("%d",&f_q);
        s_price = s_price + (160*f_q);
      }
      printf("Do your want to add more snacks (Y/N): ");
      scanf("%s",&r);
      if(r=='y'||r=='Y'){
        snacks();
      }
      else{
        break;
      }

      case 2:
        printf("Select your favorite Snacks \n");
        printf("POPCORN         Rs.150-300/- \n");
        printf("PUFFS           Rs.60/- \n");
        printf("\n");
        printf("Enter Your Choice : ");
        scanf("%d",&sn_ch);

      if(sn_ch==1){
        printf("ENTER THE SIZE : ");
        printf("1-Small     Rs.150/- \n");
        printf("2-Medium    Rs.200/- \n");
        printf("3-Large     Rs.300/- \n");
        printf("\n");
        printf("Enter number of popcorn of small/medium/large : ");
        scanf("%d%d%d",&sp_size,&mp_size,&lp_size);
        s_price= s_price + (150*sp_size)+(200*mp_size)+(300*lp_size);
        }
      else{
        printf("Enter the quantity : ");
        scanf("%d",&p_q);
        s_price = s_price + (60*p_q);
      }
      printf("Do your want to add more snacks (Y/N): ");
      scanf("%s",&r);
      if(r=='y'||r=='Y'){
        snacks();
      }
      else {
        break;
      }

      case 3:
      printf("Enter your favirote combo \n");
      printf("1. M-POPCORN + L-COKE Rs.250/- \n");
      printf("2. PUFFS + M-COKE     Rs.150/- \n");
      printf("\n");
      printf("Enter your choice : ");
      scanf("%d",&c_ch);
      if(c_ch==1){
        printf("Enter the quantity : ");
        scanf("%d",&c1_q);
        s_price = s_price + (250*c1_q);
      }
      else{
        printf("Enter the quantity : ");
        scanf("%d",&c2_q);
        s_price = s_price + (150*c2_q);
      }
      printf("Do your want to add more snacks (Y/N): ");
      scanf("%s",&r);
      if(r=='y'||r=='Y'){
        snacks();
      }
      else{
        break;
      }

      case 4:
      break;

      default:
        printf("Enter a number between 1-4");
        snacks();
    }
      
    

 printf("You should pay : Rs.%2f/- ",s_price + ticket_price);
 transaction();
}

void location(){
	printf("Available locations nearby \n");
	printf("1. Adyar \n");
  printf("2. OMR \n");
  printf("3. ECR \n");
  printf("4. Kelambakkam \n");
  printf("\n");
	printf("Enter your location:");
	scanf("%d",&loc_ch);
  
	printf("\nThe available theatres are : \n");
	if(loc_ch==1)
	 {
	   printf("Theatre A is 3km from your location \n");
	   printf("Theatre B is 7km from your location \n");
    }
  else if(loc_ch==2)
	 {
	   printf("Theatre A is 8km from your location \n");
	   printf("Theatre B is 2km from your location \n");
    }
  else if(loc_ch==3)
    {
	   printf("Theatre A is 1km from your location \n");
	   printf("Theatre B is 5km from your location \n");
    }
	else if(loc_ch==4)
	 {
	   printf("Theatre A is 6km from your location \n");
	   printf("Theatre B is 12km from your location \n");
	 }
	 else
	   printf("Invalid location \n");
  }

void transaction(){
  printf("How you like to proceed transaction \n");
  printf(" 1. Debit card \n");
  printf(" 2. Credit card \n");
  printf("\n");
  printf("\nEnter your mode of transaction:");
  scanf("%d",&trans);
  if(trans==1){
    printf("DEBIT CARD TRANSACTION \n");
    db();
  }
  else{
    printf("CREDIT CARD TRANSACTION \n");
    db();
  }
}

void db(){
  char sname[100],sno[30],otp[4];
  int mon,year,cvv;

  printf(".......... TRANSACTION........ \n");
  printf("Enter name as it appears on your card : ");
  scanf("%s",sname);
  printf("Enter your card number : ");
  scanf("%s",sno);
  printf("Enter expiry date(month&year) : ");
  scanf("%d %d",&mon,&year);
  printf("\n");
  
  printf("Enter CVV : ");
  scanf("%d",&cvv);
  if(strlen(cvv)==3){
    printf("Enter your OTP number:");
    scanf("%s",otp);
    if(strlen(otp)==4){
      printf("YOUR TRANSACTION HAS BEEN DONE SUCCESSFULLY \n");
      printf("YOUR TICKET IS BOOKED \n");
    }
    else{
      printf("YOUR TRANSACTION FAILED TRY AGAIN \n");
      transaction();
    }
  }
  else{
    printf("YOUR TRANSACTION FAILED TRY AGAIN \n");
    transaction();
  }
}

