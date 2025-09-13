<script lang="ts">
	export let data: { users: { id?: string; username?: string;}[] };
</script>

{#if data?.users?.length}
	<ul>
		{#each data.users as user (user.id)}
			<li>{user.id} ({user.username})</li>
		{/each}
	</ul>
{:else}
	<p>No users found.</p>
{/if}
