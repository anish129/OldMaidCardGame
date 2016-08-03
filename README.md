# OldMaidCardGame
# A program that executes old maid and displays winner.

package finalAnishi;

import java.util.ArrayList;
import java.util.Random;

public class OldMaid {

	// Constants for Face numeric values
	public static final Integer FACE_ACE_POINT_VALUE = 1;
	public static final Integer FACE_TWO_POINT_VALUE = 2;
	public static final Integer FACE_THREE_POINT_VALUE = 3;
	public static final Integer FACE_FOUR_POINT_VALUE = 4;
	public static final Integer FACE_FIVE_POINT_VALUE = 5;
	public static final Integer FACE_SIX_POINT_VALUE = 6;
	public static final Integer FACE_SEVEN_POINT_VALUE = 7;
	public static final Integer FACE_EIGHT_POINT_VALUE = 8;
	public static final Integer FACE_NINE_POINT_VALUE = 9;
	public static final Integer FACE_TEN_POINT_VALUE = 10;
	public static final Integer FACE_JACK_POINT_VALUE = 11;
	public static final Integer FACE_QUEEN_POINT_VALUE = 12;
	public static final Integer FACE_KING_POINT_VALUE = 13;

	// Constants for Face Name
	private static final String FACENAME_ACE = "Ace";
	private static final String FACENAME_TWO = "Two";
	private static final String FACENAME_THREE = "Three";
	private static final String FACENAME_FOUR = "Four";
	private static final String FACENAME_FIVE = "Five";
	private static final String FACENAME_SIX = "Six";
	private static final String FACENAME_SEVEN = "Seven";
	private static final String FACENAME_EIGHT = "Eight";
	private static final String FACENAME_NINE = "Nine";
	private static final String FACENAME_TEN = "Ten";
	private static final String FACENAME_JACK = "Jack";
	private static final String FACENAME_QUEEN = "Queen";
	private static final String FACENAME_KING = "King";

	// Constants for Suit numeric values
	public static final String SUIT_SPADES = "Spades";
	public static final String SUIT_CLUBS = "Clubs";
	public static final String SUIT_HEARTS = "Hearts";
	public static final String SUIT_DIAMONDS = "Diamonds";

	private int numberOfPlayers;
	ArrayList[] playerCards;

	public OldMaid(int numberOfPlayers) {
		this.numberOfPlayers = numberOfPlayers;
		playerCards = new ArrayList[numberOfPlayers];
	}

	private void dealCardsToPlayers() {
		Deck deck = getDeck(); // creates the deck of cards

		int player = 0;
		while (!deck.isEmpty()) {
			String[] card = deck.dealCard();
			if (player >= numberOfPlayers) {
				player = 0;
			}
			ArrayList<String[]> cards = playerCards[player];
			if (cards == null) {
				cards = new ArrayList<String[]>();
			}
			cards.add(card);
			playerCards[player++] = cards;
			System.out.println("Player " + player + " gets " + card[1] + " of "
					+ card[0] + " point value = " + card[2]);
		}
	}

	private Deck getDeck() {

		ArrayList<String> suits = new ArrayList<String>();
		ArrayList<String> ranks = new ArrayList<String>();
		ArrayList<Integer> pointValues = new ArrayList<Integer>();

		// Add 52 cards to the deck. All cards with the same rank has same
		// numeric value

		// Add ACE's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_ACE);
		pointValues.add(FACE_ACE_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_ACE);
		pointValues.add(FACE_ACE_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_ACE);
		pointValues.add(FACE_ACE_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_ACE);
		pointValues.add(FACE_ACE_POINT_VALUE);

		// Add the Two's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_TWO);
		pointValues.add(FACE_TWO_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_TWO);
		pointValues.add(FACE_TWO_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_TWO);
		pointValues.add(FACE_TWO_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_TWO);
		pointValues.add(FACE_TWO_POINT_VALUE);

		// Add the Three's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_THREE);
		pointValues.add(FACE_THREE_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_THREE);
		pointValues.add(FACE_THREE_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_THREE);
		pointValues.add(FACE_THREE_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_THREE);
		pointValues.add(FACE_THREE_POINT_VALUE);

		// Add the Four's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_FOUR);
		pointValues.add(FACE_FOUR_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_FOUR);
		pointValues.add(FACE_FOUR_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_FOUR);
		pointValues.add(FACE_FOUR_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_FOUR);
		pointValues.add(FACE_FOUR_POINT_VALUE);

		// Add the Five's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_FIVE);
		pointValues.add(FACE_FIVE_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_FIVE);
		pointValues.add(FACE_FIVE_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_FIVE);
		pointValues.add(FACE_FIVE_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_FIVE);
		pointValues.add(FACE_FIVE_POINT_VALUE);

		// Add the Six's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_SIX);
		pointValues.add(FACE_SIX_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_SIX);
		pointValues.add(FACE_SIX_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_SIX);
		pointValues.add(FACE_SIX_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_SIX);
		pointValues.add(FACE_SIX_POINT_VALUE);

		// Add the Seven's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_SEVEN);
		pointValues.add(FACE_SEVEN_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_SEVEN);
		pointValues.add(FACE_SEVEN_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_SEVEN);
		pointValues.add(FACE_SEVEN_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_SEVEN);
		pointValues.add(FACE_SEVEN_POINT_VALUE);

		// Add the Eight's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_EIGHT);
		pointValues.add(FACE_EIGHT_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_EIGHT);
		pointValues.add(FACE_EIGHT_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_EIGHT);
		pointValues.add(FACE_EIGHT_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_EIGHT);
		pointValues.add(FACE_EIGHT_POINT_VALUE);

		// Add the Nine's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_NINE);
		pointValues.add(FACE_NINE_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_NINE);
		pointValues.add(FACE_NINE_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_NINE);
		pointValues.add(FACE_NINE_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_NINE);
		pointValues.add(FACE_NINE_POINT_VALUE);

		// Add the Ten's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_TEN);
		pointValues.add(FACE_TEN_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_TEN);
		pointValues.add(FACE_TEN_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_TEN);
		pointValues.add(FACE_TEN_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_TEN);
		pointValues.add(FACE_TEN_POINT_VALUE);

		// Add the Jack's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_JACK);
		pointValues.add(FACE_JACK_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_JACK);
		pointValues.add(FACE_JACK_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_JACK);
		pointValues.add(FACE_JACK_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_JACK);
		pointValues.add(FACE_JACK_POINT_VALUE);

		// Add the Queen's but leaving out one

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_QUEEN);
		pointValues.add(FACE_QUEEN_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_QUEEN);
		pointValues.add(FACE_QUEEN_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_QUEEN);
		pointValues.add(FACE_QUEEN_POINT_VALUE);

		// Add the King's

		suits.add(SUIT_SPADES);
		ranks.add(FACENAME_KING);
		pointValues.add(FACE_KING_POINT_VALUE);

		suits.add(SUIT_CLUBS);
		ranks.add(FACENAME_KING);
		pointValues.add(FACE_KING_POINT_VALUE);

		suits.add(SUIT_DIAMONDS);
		ranks.add(FACENAME_KING);
		pointValues.add(FACE_KING_POINT_VALUE);

		suits.add(SUIT_HEARTS);
		ranks.add(FACENAME_KING);
		pointValues.add(FACE_KING_POINT_VALUE);

		return new Deck(suits, ranks, pointValues); // creates the deck of cards

	}

	private void play() {
		Random random = new Random();
		// deal cards
		dealCardsToPlayers();

		// let all player discard their duplicates
		int player = 1;
		for (ArrayList cards : playerCards) {
			System.out.println("Discarding duplicates for player " + player++);
			discardDuplicates(cards);
		}

		// Each player plays now
		System.out.println("Starting the game");
		int playerIndex = 0;
		while (true) {

			if (playerIndex > (numberOfPlayers - 1)) {
				playerIndex = 0;
			}

			System.out.println("Player " + (playerIndex) + " is playing");

			// get current players card list
			ArrayList currentPlayerCards = playerCards[playerIndex];

			if (currentPlayerCards.size() == 0) {
				// skip player
				playerIndex++;
				continue;
			}

			int nextPlayerIndex = playerIndex + 1;
			if (nextPlayerIndex > (numberOfPlayers - 1)) {
				nextPlayerIndex = 0;
			}

			// get next players card list
			ArrayList nextPlayerCards = playerCards[nextPlayerIndex];

			if (nextPlayerCards.size() == 0) {
				// skip player
				playerIndex++;
				continue;
			}

			// pick a random card from next players card list and remove it from
			// players list
			int randomIndex = random.nextInt(nextPlayerCards.size());
			String[] card = (String[]) nextPlayerCards.get(randomIndex);
			nextPlayerCards.remove(randomIndex);

			// add that card to curent players list
			currentPlayerCards.add(card);

			// check if current player can discard duplicates
			discardDuplicates(currentPlayerCards);

			// check if we have only one player with a card
			int numberOfPlayerWithZeroCards = 0;
			int plyrIndex = 0;
			for (ArrayList<String[]> cards : playerCards) {
				System.out.println("Player " + (plyrIndex++) + " has "
						+ cards.size() + " cards.");
				if (cards.size() == 0) {
					numberOfPlayerWithZeroCards++;
				}
			}

			if ((numberOfPlayers - numberOfPlayerWithZeroCards) == 1) {
				break;
			}

			// Move to next player
			playerIndex++;

		}
		
		ArrayList<String[]> cards = playerCards[playerIndex];
		for (String[] card : cards) {
			System.out.println("Player " + playerIndex + " has the OldMaid!");
		}

	}

	private void discardDuplicates(ArrayList<String[]> cards) {

		for (int index = 0; index < cards.size(); index++) {
			boolean cardDiscarded = false;
			String[] card = cards.get(index);
			cards.remove(index);
			System.out.println("Card is " + card[1] + " of " + card[0]);
			for (String[] remainingCard : cards) {
				// discard card with same rank
				if (remainingCard[1].equalsIgnoreCase(card[1])) {
					System.out.println("Remaining Card is " + remainingCard[1]
							+ " of " + remainingCard[0]);
					cardDiscarded = true;
					cards.remove(remainingCard);
					System.out.println(remainingCard[1] + " discarded");
					// we should discard one duplicate so break
					break;
				}
			}
			if (!cardDiscarded) {
				// put back the card
				cards.add(index, card);
			}
		}

	}

	public static void main(String[] args) {

		OldMaid game = new OldMaid(4);
		game.play();
	}

}
