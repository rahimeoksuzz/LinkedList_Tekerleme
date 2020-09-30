public class LinkList {

	private Link root;
	private Link iter;

	private class Link {

		private Link next;
		private int data;

		Link(int veri) {
			data = veri;
			next = null;
		}
	}

	public void add(int d)
	{
		Link n = new Link(d);
		if (root == null) // liste boş
		{
			iter = n;
			root = n;
		}
		else { // bir sonraki elemanı ekleriz
			iter.next = n; // bir sonraki elemanı gösterir
			iter = n;
		}

	}

	public void remove(int r)
	{
		Link d = root; Link prev = null;
		// d, başlangıç node, prev ise silindiğinde
		// bir önceki ile silindikten sonraki nodeyi bağlamak için

		while (d != null) {
			if (d.data == r) {
				if (root.data == r) { // eğer root silinecekse özel durumdur
					root = d.next;
					break;
				}
				prev.next = d.next; // normal nodelar silinirken
				d = d.next;
				break;
			}
			else { prev = d; d = d.next; } // bir sonraki nodeye geç
		}
	}

	public void print() {
		Link d = root;
		while (d != null) {
			System.out.print(d.data + " ");
			d = d.next;
		}
	}

	public static void main(String[] args)
	{

		int[] nums = { 1,2, 3 ,4 ,5,6 ,7 };
		LinkList list = new LinkList();
		for (int i = 0; i < nums.length; i++) list.add(nums[i]);


		char[] harfler = { 'a', 'e', 'ı', 'i', 'o', 'ö', 'u', 'ü' };
		//String harfler="aeıioöuü";
		char[] metin = { 'p','i','t','i','p','i','t','i','p','i','t','i','p','i','t','i','p','i','t','i','p','i','t','i' };
		int sayac = 0;
		/*
		Scanner giris=new Scanner(System.in);
		System.out.print("Metini giriniz : ");
		metin = scanner.nextLine();
		*/
		for (int i = 0; i < harfler.length; i++)
		{
			for (int j = 0; j < metin.length; j++)
			{
				if (metin[j] == harfler[i])
				{
					sayac++; //hece sayısı
				}
			}
		}
		System.out.print(sayac);

		System.out.println();
		int i = 0;
		System.out.println("OYUNCU SAYISI" + "    " + "HECE SAYISI");

		for (i = 1; i <= sayac; ++i)
		{
			System.out.println((nums.length - i) + 1 + "               " + i);
		}
		if (sayac == 1)
			list.print(); // listele
		list.remove(sayac%nums.length); //5.oyuncu silindi
		System.out.println();
		list.print(); // tekrar listele




	}

}
